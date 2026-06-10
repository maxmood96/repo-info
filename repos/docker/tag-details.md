<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.5`](#docker295)
-	[`docker:29.5-cli`](#docker295-cli)
-	[`docker:29.5-dind`](#docker295-dind)
-	[`docker:29.5-dind-rootless`](#docker295-dind-rootless)
-	[`docker:29.5-windowsservercore`](#docker295-windowsservercore)
-	[`docker:29.5-windowsservercore-ltsc2022`](#docker295-windowsservercore-ltsc2022)
-	[`docker:29.5-windowsservercore-ltsc2025`](#docker295-windowsservercore-ltsc2025)
-	[`docker:29.5.3`](#docker2953)
-	[`docker:29.5.3-alpine3.23`](#docker2953-alpine323)
-	[`docker:29.5.3-cli`](#docker2953-cli)
-	[`docker:29.5.3-cli-alpine3.23`](#docker2953-cli-alpine323)
-	[`docker:29.5.3-dind`](#docker2953-dind)
-	[`docker:29.5.3-dind-alpine3.23`](#docker2953-dind-alpine323)
-	[`docker:29.5.3-dind-rootless`](#docker2953-dind-rootless)
-	[`docker:29.5.3-windowsservercore`](#docker2953-windowsservercore)
-	[`docker:29.5.3-windowsservercore-ltsc2022`](#docker2953-windowsservercore-ltsc2022)
-	[`docker:29.5.3-windowsservercore-ltsc2025`](#docker2953-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:7d85d0eda291f1a7ab6df4a9d1802b5ad4cf9145a088bd11188c78dcb5c7392b
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
$ docker pull docker@sha256:d175bec0f43b2aabf2f1cb375d3a0a5b540d60f82d3396dd473c835dea3525b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141571380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a47c98f97ef56a4b9ccfd268e6cc88eed4977222b3b66075165a05af9813e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:90d0717771cb46fea9e5335b4faf6b7fffffb29a8569967229f367338c4713c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0096914d04c0764856dcac037cc382383886bffdf3f73cbde86d3d89b5e25a`

```dockerfile
```

-	Layers:
	-	`sha256:8f74a25397fb78ec243dd8da45e2a676a6871587708f136f2b937886d980e124`  
		Last Modified: Thu, 04 Jun 2026 18:12:52 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:cccfdafc9b7735790124fc5ce0179ba190af4bfa1267ee56c21b069b0aa9b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133489319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3dd3e0f3eda4e49328697e623bcb5c2c4aa5a765ae25eb08fef63af492c8e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:49 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9698419a4fcfcfe53d39266385d0bdeadd8e3982c4c56be06088441af10d9d1a`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 7.3 MB (7278696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590d2829119f18520f97f8a0e744c191ca689d56c3945b532a37f4a1f57bf4f8`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 91.5 KB (91513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83f5308195cac080d9b65d0a2011263997412b414d259f7ad52d623c63a331`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd583d84ca571dbaf9008bdbaeae8371155aa2b4ead91c47494a7b421553b`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 64.0 MB (63954789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d3a29cd4fa1b4ca8c9a8bba57b6adec84495c4691cbf0a667f171ff9e49bd`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164bf1f4aad38e26ea7f523c0b8cd2508f1df7d8f39d65013f5e6b8a96ba3da`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:d1df1fb1e10855a2303e6295a1a17659f195d1845fc09ba6710eab2a82fa395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d89fb7855e5bc3e7e32727270386dd28a4f65936c4c472149c4c948063727`

```dockerfile
```

-	Layers:
	-	`sha256:81063e8f5ff0dc3d078be22a68c6973cfac7b866b95065c07c7597fff545894d`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:abd9432e46604318976d12dcb044b176e5a31ced7060b18602d42b54de200335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131594459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d33334019c68c6d9d380d7af58f0be8dbf0ae991cda104cd600dc29c2438e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3d7d1e69bcb16737aba3f84171773e55dc5e7293ab857fbbc754e0b61c181`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 6.6 MB (6577156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35895177edcf0459851a68da3f529aad815c6a06fc487bc78b67925822656c2`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 87.8 KB (87838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76012c6359cf96274f94e94ff4d395f8dcc9562130981ad47924978054b0f083`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a191244d67d45d9772df793ae4c4569cc18daab0aa247288428000db7a4e0a03`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 63.8 MB (63785660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0234b9f18f3e4e53673b485b84b67f0a658a88dc1de10bfe728995844996b`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad57512870cbfde869dda3537d23c6d1056b25b0243b1f2823b31e8771f9a2c`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:355b3babed5e09d804da8c33da9f3ed53746277aab8c1e43ecbe44c04cd09668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ccef25134c4f167d669bb33f7132a58a52e45c33d569d7679cdb81f001e0ff`

```dockerfile
```

-	Layers:
	-	`sha256:4eebc04a44848f48946a6c5a194b0c366123dae69712777b204e003616fecb18`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:387297c81bd1610b71e90a377ef6306f213d9262387b4d23883481a1f90a2550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130978501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ab87dbef3dcba50bd1de84ab87396a610d1281dba6f3e67f8ce5452fb2f67`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:d8a2f66d8cb21198f3c009790c921dd7f1940c10a3ad9d0235741829eb140e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7de24f830a299a1e537977495fbf842b9d31f3e70750c2f2ecd7c274283b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f227e53b9e53c71cc3a11d1d3c57f48e6fbdff69b2751016ea87727251e354e1`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:873de13208aab9c1de73fe984fd45883e01464fcfcc85efa20aa56a9ccfe7aa6
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
$ docker pull docker@sha256:d76a30ee8d7cc923cead6aef3e7b2b95ed8754dea7701f710d15e1fae1f70665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65862792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a00d98eb41b3144ec842f155d2688a13ed80d2fc5f1f70a8f73248d2e6f7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6923fa5011619a2d94dfb1d4ff853ff03adf7f2db967aa38854e8f4d47a067e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f22e60f4675b6e66a56713df1f73b70380a77fe284aaa7cf701b071382461f`

```dockerfile
```

-	Layers:
	-	`sha256:04ca03ce00ea392caae12cb4c437840b47f287abebf1d1dbf3a5bad2da881c8d`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:5bfff669277f7f9697c38c252600c46a60e34d6dcedbb6f23c1d37021555a2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62158321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ecff33f7643bd23d957b4136eff32e8ebac9add92b386c892caab32be32042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:383aab319724e2859039621d73e694f182f9804c673086928157477a580a8adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bc17dd1dec2758cdbc234dc801c256d93ec2ba6d3f5620c7dba50d7bf5943b`

```dockerfile
```

-	Layers:
	-	`sha256:e972de05273404ea4cc8d372a1b113a32138268f654e03e9a634ec9b338340c7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:902b3e5d8c1f3a8f50df537a2d569ec5369f96b8d7b47c4526a76e361f367297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61137803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927d1990201b745cb2b5c668aababaeac90c8053616f76665b152acf4c1d18ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d25246c6f6f19bc2d7bb5f113477aa78b540f39b79c54a54eed995e41fcd92b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a4d350556ced6cd5503c4b47b535e4f06598f7367f1a371a6050dec513a4c3`

```dockerfile
```

-	Layers:
	-	`sha256:974a2f1fef10826b93c3c467378744a0c7908059cc0c94c9493ead2bee490f37`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ed88538a7eb93cfa5e57b33d6544c182d423e7b55495f4f145896259bdbad899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61510517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a955ea7748f070ef6668ad2f79a466fa47e5ba52025c119d633d0be050605c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:566af4ebd5051b461ee31eba5e3e542993b993ea4553c8483383c2c5b38a7a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2462c1f7883cf00b4a0f6799aa4b5df7b02a32feacb94d8f8f4ce0969fc36d81`

```dockerfile
```

-	Layers:
	-	`sha256:d8cf46622fa8d5f46e8102daf4afbb68603f2bfd7a634800c67c95401a52a104`  
		Last Modified: Thu, 04 Jun 2026 18:07:58 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:7d85d0eda291f1a7ab6df4a9d1802b5ad4cf9145a088bd11188c78dcb5c7392b
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
$ docker pull docker@sha256:d175bec0f43b2aabf2f1cb375d3a0a5b540d60f82d3396dd473c835dea3525b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141571380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a47c98f97ef56a4b9ccfd268e6cc88eed4977222b3b66075165a05af9813e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:90d0717771cb46fea9e5335b4faf6b7fffffb29a8569967229f367338c4713c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0096914d04c0764856dcac037cc382383886bffdf3f73cbde86d3d89b5e25a`

```dockerfile
```

-	Layers:
	-	`sha256:8f74a25397fb78ec243dd8da45e2a676a6871587708f136f2b937886d980e124`  
		Last Modified: Thu, 04 Jun 2026 18:12:52 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:cccfdafc9b7735790124fc5ce0179ba190af4bfa1267ee56c21b069b0aa9b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133489319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3dd3e0f3eda4e49328697e623bcb5c2c4aa5a765ae25eb08fef63af492c8e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:49 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9698419a4fcfcfe53d39266385d0bdeadd8e3982c4c56be06088441af10d9d1a`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 7.3 MB (7278696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590d2829119f18520f97f8a0e744c191ca689d56c3945b532a37f4a1f57bf4f8`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 91.5 KB (91513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83f5308195cac080d9b65d0a2011263997412b414d259f7ad52d623c63a331`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd583d84ca571dbaf9008bdbaeae8371155aa2b4ead91c47494a7b421553b`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 64.0 MB (63954789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d3a29cd4fa1b4ca8c9a8bba57b6adec84495c4691cbf0a667f171ff9e49bd`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164bf1f4aad38e26ea7f523c0b8cd2508f1df7d8f39d65013f5e6b8a96ba3da`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d1df1fb1e10855a2303e6295a1a17659f195d1845fc09ba6710eab2a82fa395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d89fb7855e5bc3e7e32727270386dd28a4f65936c4c472149c4c948063727`

```dockerfile
```

-	Layers:
	-	`sha256:81063e8f5ff0dc3d078be22a68c6973cfac7b866b95065c07c7597fff545894d`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:abd9432e46604318976d12dcb044b176e5a31ced7060b18602d42b54de200335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131594459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d33334019c68c6d9d380d7af58f0be8dbf0ae991cda104cd600dc29c2438e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3d7d1e69bcb16737aba3f84171773e55dc5e7293ab857fbbc754e0b61c181`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 6.6 MB (6577156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35895177edcf0459851a68da3f529aad815c6a06fc487bc78b67925822656c2`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 87.8 KB (87838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76012c6359cf96274f94e94ff4d395f8dcc9562130981ad47924978054b0f083`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a191244d67d45d9772df793ae4c4569cc18daab0aa247288428000db7a4e0a03`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 63.8 MB (63785660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0234b9f18f3e4e53673b485b84b67f0a658a88dc1de10bfe728995844996b`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad57512870cbfde869dda3537d23c6d1056b25b0243b1f2823b31e8771f9a2c`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:355b3babed5e09d804da8c33da9f3ed53746277aab8c1e43ecbe44c04cd09668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ccef25134c4f167d669bb33f7132a58a52e45c33d569d7679cdb81f001e0ff`

```dockerfile
```

-	Layers:
	-	`sha256:4eebc04a44848f48946a6c5a194b0c366123dae69712777b204e003616fecb18`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:387297c81bd1610b71e90a377ef6306f213d9262387b4d23883481a1f90a2550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130978501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ab87dbef3dcba50bd1de84ab87396a610d1281dba6f3e67f8ce5452fb2f67`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d8a2f66d8cb21198f3c009790c921dd7f1940c10a3ad9d0235741829eb140e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7de24f830a299a1e537977495fbf842b9d31f3e70750c2f2ecd7c274283b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f227e53b9e53c71cc3a11d1d3c57f48e6fbdff69b2751016ea87727251e354e1`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:41825fb12da6b78219af4b862830f252be1f5dee3d6cbfd508736ed31c0014d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9f5c3cc894bf49af0667c5b2662b9a4f309d079aa0337324bdca7b748e964876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157096105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b737c7bee606e4bc72ac59c92d9b4d8dd1d2dc020ac6619938ab8d25579309e4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
# Thu, 04 Jun 2026 18:14:30 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Jun 2026 18:14:30 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Jun 2026 18:14:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Jun 2026 18:14:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2db229f6b5fa1fd732d8fba1e949c5c7e73e730e16357c16495923eb4de021c`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 3.4 MB (3420079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bd807b36584452264c40c10ca5b43c04108f21f4a61575c208ad0f6fcea4c3`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d4aff48ac38b7051cfccbdaced29f5b735a83a9f6387ccfe30cc5fd7b83084`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8974b16bb9e50c8552367b5aba959a7bdd24079a8b84430486638e82c3c02ff`  
		Last Modified: Thu, 04 Jun 2026 18:14:37 GMT  
		Size: 12.1 MB (12103307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad90cb2bc6565f2bfe4570ff4400df96b165f0c295dfae388f2b502aaf504ec`  
		Last Modified: Thu, 04 Jun 2026 18:14:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:210086fd9e446a787d03d83b9f6d28e95bd05fc7b752495c6ad1b684e7a5107f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239d1603cd7d20cf2b717faedf8a6799cb79831f582f00904a69213db49adb`

```dockerfile
```

-	Layers:
	-	`sha256:3605fd3d07b5c864bed987b1cf0900c688cb6b5a4886cd6e9eaf96384171485c`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 30.5 KB (30492 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b61013cc22712072617daa3684a4b51259ee5b5b9a5e1cb31958ebda52b6a697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145611456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46aee58794f1f1bb31fcc972c975b297b4970c7f6b648186ff66800511ed2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
# Thu, 04 Jun 2026 18:14:37 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Jun 2026 18:14:37 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e24e15f563ca4ef38267a4ece0cde7eb2ea2b6c71439f2f8ad3e681bf0dc8c`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 3.4 MB (3394532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd56f3c1721d727b2bb80a572d12001a4da9f269d19ca40ba68f13201572e54`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98aaab4cf1e555e08f7d5aac3445aab4317f29393ae87857469d74d15e942de`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938547d0fb3967e62653e6b2649c8dfc048576f66f32576f7432a81466be2fcb`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 11.2 MB (11237084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d35d5c447eb8a4e37a5670c1c0b25137c3d27f3bd6a58b34de7f8df41959c2`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c2743e70adcc0e287ee4767cc6b01965cd3e1298f2f2b97bb5583213e323bff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d7ef8ce3af550022eb687e4d68f22fcb3f28226bd5c9c481cccba58d5ad5ad`

```dockerfile
```

-	Layers:
	-	`sha256:dd88782a3b7d95075d0232118200d547b991e9eb5674d30ca0febba0efc0cafe`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:a4506ea88c29d83e0c6f74a20dde3d510d490377feb330023763fc4180ede82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:626792a62ccf43d2c9c9f4106f25ac02fc10678a0f7ba40048484f76cccceb88
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335542989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9b36b1ba1723e3254afdfda83f60d48a67f885c462964ad4e4c9e14caea0a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:08:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:10:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:10:06 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:25 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:46 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:11:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e863137cc1a6c081981346b9911aa1b849767470cdb83cf8038b653b226e5`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13126202d74ea043ab743e8c58bf13f03d98c23877900c616afdb1fcb05ffc`  
		Last Modified: Tue, 09 Jun 2026 22:11:10 GMT  
		Size: 366.6 KB (366612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8450b716d93cc1abde208e2b7bbf780e835eedac6e83b3bf107dd22257e6d4f3`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0798499ee10239ba25cc04fb9b50137e1dc8535b2f0f7d8ec34d61a24e4334`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4335418e7b397c58162055ace3d049acef6d6a75695d40dcf7e1db5adcddc0e4`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 20.0 MB (20005460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82583ec76facc4e8c5d476866755314aac071c25b88ccc0714a9ea28cb9d5916`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c320c84b185908993c2ae455c8e19c447a3440d143e3df1e530688c2f2e48ab`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de253f20eb848fe03012cde3845923b7c3cbd8109b8848bcc65fe1a7e8ec78db`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1070177e1931be03c0bd9b077e590d23aba398d31e78f470b4a25895543ca9`  
		Last Modified: Tue, 09 Jun 2026 22:11:13 GMT  
		Size: 23.9 MB (23917170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44aca9e4206f912e275df50b300bb51b33594cb83228092fd0a1d7fda852d13`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09348bd8a2ac253880aff66aafdd100a7937ef94ecbd671ba62ea967a391c583`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0907212d8ad1bf4caaf2f7d9bae2ab4b6f11ce4bf246f2b3342a04b587941720`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d7087beffaf8878b9474aa75e2c3f844499000ed25a49af03ed7cf6ce3a487`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 12.1 MB (12099197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:e1874ace86696dc406093e614d34ce6a6f07ed7187e25f029685911a711ccc40
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188548521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d76e268d68e640ffd98a8af27bf187fba7876b6ac6253c294854ec499aed056`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:09:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:09:41 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:09:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:09 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:39 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:10:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a21107eb392ad352a11d88add9657687384931e5d889cdcf2e9933b4421077`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b0d166672182721ce571506f9d6ffbdf3978263c1e98a8c7cb83d70e5ceb3`  
		Last Modified: Tue, 09 Jun 2026 22:10:56 GMT  
		Size: 487.8 KB (487761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b460336fce54b4157c40e9e971fab0f408aeda838dde55bcf5ea5de52f3fa3`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea67caacc1b68dc837ec089a76c72de278a12c98986a9e7e27a6b4fa3f1f289`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9755d22906699b3ae49e1e7e643b80a71128ccb86715598896d101848d5074`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 20.0 MB (19967046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa89af8ddf8470a85bb4691fdf78f932741c527c8b8f25d9cdb0ab957b72766`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e31ea216b5955db20bf270de50921353f50fb244567aeffa9aec6a22bdf910`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0473ee7061cd54cff9f36e7d95856e8a0ad754f1afd89c20cff85132b100c5f`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d1bb31a8a58e6c19fa9476763d11417da6c9deccc5f3a25491e741f79611`  
		Last Modified: Tue, 09 Jun 2026 22:11:00 GMT  
		Size: 23.9 MB (23888859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e4bdf749ee7ad62af795111680dbce48097a254a3d53ebee0f0feb07f3820`  
		Last Modified: Tue, 09 Jun 2026 22:10:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdcd68b54960c0145901d3e97fbca29555cdd34359f1433932b88715f7ebd8a`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcecc97fe08a6e5f535dbb042a7e39cee7fd26ff6b8f64f4b87657d71a9ca42`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057fa34c824943d81b41f22bf794e23e40378d1db98addd0261c1fc64a152f55`  
		Last Modified: Tue, 09 Jun 2026 22:10:54 GMT  
		Size: 12.1 MB (12067581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9df2b61e3220bc07763d0d46ea3ea7d312e1e012d5c746cf9686ca44cd8b59cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:e1874ace86696dc406093e614d34ce6a6f07ed7187e25f029685911a711ccc40
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188548521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d76e268d68e640ffd98a8af27bf187fba7876b6ac6253c294854ec499aed056`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:09:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:09:41 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:09:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:09 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:39 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:10:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a21107eb392ad352a11d88add9657687384931e5d889cdcf2e9933b4421077`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b0d166672182721ce571506f9d6ffbdf3978263c1e98a8c7cb83d70e5ceb3`  
		Last Modified: Tue, 09 Jun 2026 22:10:56 GMT  
		Size: 487.8 KB (487761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b460336fce54b4157c40e9e971fab0f408aeda838dde55bcf5ea5de52f3fa3`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea67caacc1b68dc837ec089a76c72de278a12c98986a9e7e27a6b4fa3f1f289`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9755d22906699b3ae49e1e7e643b80a71128ccb86715598896d101848d5074`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 20.0 MB (19967046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa89af8ddf8470a85bb4691fdf78f932741c527c8b8f25d9cdb0ab957b72766`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e31ea216b5955db20bf270de50921353f50fb244567aeffa9aec6a22bdf910`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0473ee7061cd54cff9f36e7d95856e8a0ad754f1afd89c20cff85132b100c5f`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d1bb31a8a58e6c19fa9476763d11417da6c9deccc5f3a25491e741f79611`  
		Last Modified: Tue, 09 Jun 2026 22:11:00 GMT  
		Size: 23.9 MB (23888859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e4bdf749ee7ad62af795111680dbce48097a254a3d53ebee0f0feb07f3820`  
		Last Modified: Tue, 09 Jun 2026 22:10:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdcd68b54960c0145901d3e97fbca29555cdd34359f1433932b88715f7ebd8a`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcecc97fe08a6e5f535dbb042a7e39cee7fd26ff6b8f64f4b87657d71a9ca42`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057fa34c824943d81b41f22bf794e23e40378d1db98addd0261c1fc64a152f55`  
		Last Modified: Tue, 09 Jun 2026 22:10:54 GMT  
		Size: 12.1 MB (12067581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b641303b79f48efd2803ac9c593cdd44c95c59202eb8d7e4380fa6caf293430b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:626792a62ccf43d2c9c9f4106f25ac02fc10678a0f7ba40048484f76cccceb88
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335542989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9b36b1ba1723e3254afdfda83f60d48a67f885c462964ad4e4c9e14caea0a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:08:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:10:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:10:06 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:25 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:46 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:11:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e863137cc1a6c081981346b9911aa1b849767470cdb83cf8038b653b226e5`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13126202d74ea043ab743e8c58bf13f03d98c23877900c616afdb1fcb05ffc`  
		Last Modified: Tue, 09 Jun 2026 22:11:10 GMT  
		Size: 366.6 KB (366612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8450b716d93cc1abde208e2b7bbf780e835eedac6e83b3bf107dd22257e6d4f3`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0798499ee10239ba25cc04fb9b50137e1dc8535b2f0f7d8ec34d61a24e4334`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4335418e7b397c58162055ace3d049acef6d6a75695d40dcf7e1db5adcddc0e4`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 20.0 MB (20005460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82583ec76facc4e8c5d476866755314aac071c25b88ccc0714a9ea28cb9d5916`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c320c84b185908993c2ae455c8e19c447a3440d143e3df1e530688c2f2e48ab`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de253f20eb848fe03012cde3845923b7c3cbd8109b8848bcc65fe1a7e8ec78db`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1070177e1931be03c0bd9b077e590d23aba398d31e78f470b4a25895543ca9`  
		Last Modified: Tue, 09 Jun 2026 22:11:13 GMT  
		Size: 23.9 MB (23917170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44aca9e4206f912e275df50b300bb51b33594cb83228092fd0a1d7fda852d13`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09348bd8a2ac253880aff66aafdd100a7937ef94ecbd671ba62ea967a391c583`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0907212d8ad1bf4caaf2f7d9bae2ab4b6f11ce4bf246f2b3342a04b587941720`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d7087beffaf8878b9474aa75e2c3f844499000ed25a49af03ed7cf6ce3a487`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 12.1 MB (12099197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5`

```console
$ docker pull docker@sha256:7d85d0eda291f1a7ab6df4a9d1802b5ad4cf9145a088bd11188c78dcb5c7392b
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

### `docker:29.5` - linux; amd64

```console
$ docker pull docker@sha256:d175bec0f43b2aabf2f1cb375d3a0a5b540d60f82d3396dd473c835dea3525b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141571380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a47c98f97ef56a4b9ccfd268e6cc88eed4977222b3b66075165a05af9813e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5` - unknown; unknown

```console
$ docker pull docker@sha256:90d0717771cb46fea9e5335b4faf6b7fffffb29a8569967229f367338c4713c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0096914d04c0764856dcac037cc382383886bffdf3f73cbde86d3d89b5e25a`

```dockerfile
```

-	Layers:
	-	`sha256:8f74a25397fb78ec243dd8da45e2a676a6871587708f136f2b937886d980e124`  
		Last Modified: Thu, 04 Jun 2026 18:12:52 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5` - linux; arm variant v6

```console
$ docker pull docker@sha256:cccfdafc9b7735790124fc5ce0179ba190af4bfa1267ee56c21b069b0aa9b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133489319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3dd3e0f3eda4e49328697e623bcb5c2c4aa5a765ae25eb08fef63af492c8e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:49 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9698419a4fcfcfe53d39266385d0bdeadd8e3982c4c56be06088441af10d9d1a`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 7.3 MB (7278696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590d2829119f18520f97f8a0e744c191ca689d56c3945b532a37f4a1f57bf4f8`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 91.5 KB (91513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83f5308195cac080d9b65d0a2011263997412b414d259f7ad52d623c63a331`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd583d84ca571dbaf9008bdbaeae8371155aa2b4ead91c47494a7b421553b`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 64.0 MB (63954789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d3a29cd4fa1b4ca8c9a8bba57b6adec84495c4691cbf0a667f171ff9e49bd`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164bf1f4aad38e26ea7f523c0b8cd2508f1df7d8f39d65013f5e6b8a96ba3da`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5` - unknown; unknown

```console
$ docker pull docker@sha256:d1df1fb1e10855a2303e6295a1a17659f195d1845fc09ba6710eab2a82fa395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d89fb7855e5bc3e7e32727270386dd28a4f65936c4c472149c4c948063727`

```dockerfile
```

-	Layers:
	-	`sha256:81063e8f5ff0dc3d078be22a68c6973cfac7b866b95065c07c7597fff545894d`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5` - linux; arm variant v7

```console
$ docker pull docker@sha256:abd9432e46604318976d12dcb044b176e5a31ced7060b18602d42b54de200335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131594459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d33334019c68c6d9d380d7af58f0be8dbf0ae991cda104cd600dc29c2438e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3d7d1e69bcb16737aba3f84171773e55dc5e7293ab857fbbc754e0b61c181`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 6.6 MB (6577156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35895177edcf0459851a68da3f529aad815c6a06fc487bc78b67925822656c2`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 87.8 KB (87838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76012c6359cf96274f94e94ff4d395f8dcc9562130981ad47924978054b0f083`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a191244d67d45d9772df793ae4c4569cc18daab0aa247288428000db7a4e0a03`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 63.8 MB (63785660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0234b9f18f3e4e53673b485b84b67f0a658a88dc1de10bfe728995844996b`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad57512870cbfde869dda3537d23c6d1056b25b0243b1f2823b31e8771f9a2c`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5` - unknown; unknown

```console
$ docker pull docker@sha256:355b3babed5e09d804da8c33da9f3ed53746277aab8c1e43ecbe44c04cd09668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ccef25134c4f167d669bb33f7132a58a52e45c33d569d7679cdb81f001e0ff`

```dockerfile
```

-	Layers:
	-	`sha256:4eebc04a44848f48946a6c5a194b0c366123dae69712777b204e003616fecb18`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:387297c81bd1610b71e90a377ef6306f213d9262387b4d23883481a1f90a2550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130978501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ab87dbef3dcba50bd1de84ab87396a610d1281dba6f3e67f8ce5452fb2f67`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5` - unknown; unknown

```console
$ docker pull docker@sha256:d8a2f66d8cb21198f3c009790c921dd7f1940c10a3ad9d0235741829eb140e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7de24f830a299a1e537977495fbf842b9d31f3e70750c2f2ecd7c274283b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f227e53b9e53c71cc3a11d1d3c57f48e6fbdff69b2751016ea87727251e354e1`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-cli`

```console
$ docker pull docker@sha256:873de13208aab9c1de73fe984fd45883e01464fcfcc85efa20aa56a9ccfe7aa6
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

### `docker:29.5-cli` - linux; amd64

```console
$ docker pull docker@sha256:d76a30ee8d7cc923cead6aef3e7b2b95ed8754dea7701f710d15e1fae1f70665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65862792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a00d98eb41b3144ec842f155d2688a13ed80d2fc5f1f70a8f73248d2e6f7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6923fa5011619a2d94dfb1d4ff853ff03adf7f2db967aa38854e8f4d47a067e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f22e60f4675b6e66a56713df1f73b70380a77fe284aaa7cf701b071382461f`

```dockerfile
```

-	Layers:
	-	`sha256:04ca03ce00ea392caae12cb4c437840b47f287abebf1d1dbf3a5bad2da881c8d`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:5bfff669277f7f9697c38c252600c46a60e34d6dcedbb6f23c1d37021555a2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62158321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ecff33f7643bd23d957b4136eff32e8ebac9add92b386c892caab32be32042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:383aab319724e2859039621d73e694f182f9804c673086928157477a580a8adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bc17dd1dec2758cdbc234dc801c256d93ec2ba6d3f5620c7dba50d7bf5943b`

```dockerfile
```

-	Layers:
	-	`sha256:e972de05273404ea4cc8d372a1b113a32138268f654e03e9a634ec9b338340c7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:902b3e5d8c1f3a8f50df537a2d569ec5369f96b8d7b47c4526a76e361f367297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61137803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927d1990201b745cb2b5c668aababaeac90c8053616f76665b152acf4c1d18ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d25246c6f6f19bc2d7bb5f113477aa78b540f39b79c54a54eed995e41fcd92b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a4d350556ced6cd5503c4b47b535e4f06598f7367f1a371a6050dec513a4c3`

```dockerfile
```

-	Layers:
	-	`sha256:974a2f1fef10826b93c3c467378744a0c7908059cc0c94c9493ead2bee490f37`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ed88538a7eb93cfa5e57b33d6544c182d423e7b55495f4f145896259bdbad899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61510517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a955ea7748f070ef6668ad2f79a466fa47e5ba52025c119d633d0be050605c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:566af4ebd5051b461ee31eba5e3e542993b993ea4553c8483383c2c5b38a7a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2462c1f7883cf00b4a0f6799aa4b5df7b02a32feacb94d8f8f4ce0969fc36d81`

```dockerfile
```

-	Layers:
	-	`sha256:d8cf46622fa8d5f46e8102daf4afbb68603f2bfd7a634800c67c95401a52a104`  
		Last Modified: Thu, 04 Jun 2026 18:07:58 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-dind`

```console
$ docker pull docker@sha256:7d85d0eda291f1a7ab6df4a9d1802b5ad4cf9145a088bd11188c78dcb5c7392b
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

### `docker:29.5-dind` - linux; amd64

```console
$ docker pull docker@sha256:d175bec0f43b2aabf2f1cb375d3a0a5b540d60f82d3396dd473c835dea3525b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141571380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a47c98f97ef56a4b9ccfd268e6cc88eed4977222b3b66075165a05af9813e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:90d0717771cb46fea9e5335b4faf6b7fffffb29a8569967229f367338c4713c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0096914d04c0764856dcac037cc382383886bffdf3f73cbde86d3d89b5e25a`

```dockerfile
```

-	Layers:
	-	`sha256:8f74a25397fb78ec243dd8da45e2a676a6871587708f136f2b937886d980e124`  
		Last Modified: Thu, 04 Jun 2026 18:12:52 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:cccfdafc9b7735790124fc5ce0179ba190af4bfa1267ee56c21b069b0aa9b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133489319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3dd3e0f3eda4e49328697e623bcb5c2c4aa5a765ae25eb08fef63af492c8e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:49 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9698419a4fcfcfe53d39266385d0bdeadd8e3982c4c56be06088441af10d9d1a`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 7.3 MB (7278696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590d2829119f18520f97f8a0e744c191ca689d56c3945b532a37f4a1f57bf4f8`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 91.5 KB (91513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83f5308195cac080d9b65d0a2011263997412b414d259f7ad52d623c63a331`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd583d84ca571dbaf9008bdbaeae8371155aa2b4ead91c47494a7b421553b`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 64.0 MB (63954789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d3a29cd4fa1b4ca8c9a8bba57b6adec84495c4691cbf0a667f171ff9e49bd`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164bf1f4aad38e26ea7f523c0b8cd2508f1df7d8f39d65013f5e6b8a96ba3da`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d1df1fb1e10855a2303e6295a1a17659f195d1845fc09ba6710eab2a82fa395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d89fb7855e5bc3e7e32727270386dd28a4f65936c4c472149c4c948063727`

```dockerfile
```

-	Layers:
	-	`sha256:81063e8f5ff0dc3d078be22a68c6973cfac7b866b95065c07c7597fff545894d`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:abd9432e46604318976d12dcb044b176e5a31ced7060b18602d42b54de200335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131594459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d33334019c68c6d9d380d7af58f0be8dbf0ae991cda104cd600dc29c2438e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3d7d1e69bcb16737aba3f84171773e55dc5e7293ab857fbbc754e0b61c181`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 6.6 MB (6577156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35895177edcf0459851a68da3f529aad815c6a06fc487bc78b67925822656c2`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 87.8 KB (87838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76012c6359cf96274f94e94ff4d395f8dcc9562130981ad47924978054b0f083`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a191244d67d45d9772df793ae4c4569cc18daab0aa247288428000db7a4e0a03`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 63.8 MB (63785660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0234b9f18f3e4e53673b485b84b67f0a658a88dc1de10bfe728995844996b`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad57512870cbfde869dda3537d23c6d1056b25b0243b1f2823b31e8771f9a2c`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:355b3babed5e09d804da8c33da9f3ed53746277aab8c1e43ecbe44c04cd09668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ccef25134c4f167d669bb33f7132a58a52e45c33d569d7679cdb81f001e0ff`

```dockerfile
```

-	Layers:
	-	`sha256:4eebc04a44848f48946a6c5a194b0c366123dae69712777b204e003616fecb18`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:387297c81bd1610b71e90a377ef6306f213d9262387b4d23883481a1f90a2550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130978501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ab87dbef3dcba50bd1de84ab87396a610d1281dba6f3e67f8ce5452fb2f67`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d8a2f66d8cb21198f3c009790c921dd7f1940c10a3ad9d0235741829eb140e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7de24f830a299a1e537977495fbf842b9d31f3e70750c2f2ecd7c274283b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f227e53b9e53c71cc3a11d1d3c57f48e6fbdff69b2751016ea87727251e354e1`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-dind-rootless`

```console
$ docker pull docker@sha256:41825fb12da6b78219af4b862830f252be1f5dee3d6cbfd508736ed31c0014d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.5-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9f5c3cc894bf49af0667c5b2662b9a4f309d079aa0337324bdca7b748e964876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157096105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b737c7bee606e4bc72ac59c92d9b4d8dd1d2dc020ac6619938ab8d25579309e4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
# Thu, 04 Jun 2026 18:14:30 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Jun 2026 18:14:30 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Jun 2026 18:14:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Jun 2026 18:14:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2db229f6b5fa1fd732d8fba1e949c5c7e73e730e16357c16495923eb4de021c`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 3.4 MB (3420079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bd807b36584452264c40c10ca5b43c04108f21f4a61575c208ad0f6fcea4c3`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d4aff48ac38b7051cfccbdaced29f5b735a83a9f6387ccfe30cc5fd7b83084`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8974b16bb9e50c8552367b5aba959a7bdd24079a8b84430486638e82c3c02ff`  
		Last Modified: Thu, 04 Jun 2026 18:14:37 GMT  
		Size: 12.1 MB (12103307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad90cb2bc6565f2bfe4570ff4400df96b165f0c295dfae388f2b502aaf504ec`  
		Last Modified: Thu, 04 Jun 2026 18:14:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:210086fd9e446a787d03d83b9f6d28e95bd05fc7b752495c6ad1b684e7a5107f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239d1603cd7d20cf2b717faedf8a6799cb79831f582f00904a69213db49adb`

```dockerfile
```

-	Layers:
	-	`sha256:3605fd3d07b5c864bed987b1cf0900c688cb6b5a4886cd6e9eaf96384171485c`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 30.5 KB (30492 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b61013cc22712072617daa3684a4b51259ee5b5b9a5e1cb31958ebda52b6a697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145611456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46aee58794f1f1bb31fcc972c975b297b4970c7f6b648186ff66800511ed2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
# Thu, 04 Jun 2026 18:14:37 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Jun 2026 18:14:37 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e24e15f563ca4ef38267a4ece0cde7eb2ea2b6c71439f2f8ad3e681bf0dc8c`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 3.4 MB (3394532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd56f3c1721d727b2bb80a572d12001a4da9f269d19ca40ba68f13201572e54`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98aaab4cf1e555e08f7d5aac3445aab4317f29393ae87857469d74d15e942de`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938547d0fb3967e62653e6b2649c8dfc048576f66f32576f7432a81466be2fcb`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 11.2 MB (11237084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d35d5c447eb8a4e37a5670c1c0b25137c3d27f3bd6a58b34de7f8df41959c2`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c2743e70adcc0e287ee4767cc6b01965cd3e1298f2f2b97bb5583213e323bff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d7ef8ce3af550022eb687e4d68f22fcb3f28226bd5c9c481cccba58d5ad5ad`

```dockerfile
```

-	Layers:
	-	`sha256:dd88782a3b7d95075d0232118200d547b991e9eb5674d30ca0febba0efc0cafe`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-windowsservercore`

```console
$ docker pull docker@sha256:a4506ea88c29d83e0c6f74a20dde3d510d490377feb330023763fc4180ede82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `docker:29.5-windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:626792a62ccf43d2c9c9f4106f25ac02fc10678a0f7ba40048484f76cccceb88
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335542989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9b36b1ba1723e3254afdfda83f60d48a67f885c462964ad4e4c9e14caea0a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:08:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:10:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:10:06 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:25 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:46 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:11:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e863137cc1a6c081981346b9911aa1b849767470cdb83cf8038b653b226e5`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13126202d74ea043ab743e8c58bf13f03d98c23877900c616afdb1fcb05ffc`  
		Last Modified: Tue, 09 Jun 2026 22:11:10 GMT  
		Size: 366.6 KB (366612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8450b716d93cc1abde208e2b7bbf780e835eedac6e83b3bf107dd22257e6d4f3`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0798499ee10239ba25cc04fb9b50137e1dc8535b2f0f7d8ec34d61a24e4334`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4335418e7b397c58162055ace3d049acef6d6a75695d40dcf7e1db5adcddc0e4`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 20.0 MB (20005460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82583ec76facc4e8c5d476866755314aac071c25b88ccc0714a9ea28cb9d5916`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c320c84b185908993c2ae455c8e19c447a3440d143e3df1e530688c2f2e48ab`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de253f20eb848fe03012cde3845923b7c3cbd8109b8848bcc65fe1a7e8ec78db`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1070177e1931be03c0bd9b077e590d23aba398d31e78f470b4a25895543ca9`  
		Last Modified: Tue, 09 Jun 2026 22:11:13 GMT  
		Size: 23.9 MB (23917170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44aca9e4206f912e275df50b300bb51b33594cb83228092fd0a1d7fda852d13`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09348bd8a2ac253880aff66aafdd100a7937ef94ecbd671ba62ea967a391c583`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0907212d8ad1bf4caaf2f7d9bae2ab4b6f11ce4bf246f2b3342a04b587941720`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d7087beffaf8878b9474aa75e2c3f844499000ed25a49af03ed7cf6ce3a487`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 12.1 MB (12099197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.5-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:e1874ace86696dc406093e614d34ce6a6f07ed7187e25f029685911a711ccc40
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188548521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d76e268d68e640ffd98a8af27bf187fba7876b6ac6253c294854ec499aed056`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:09:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:09:41 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:09:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:09 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:39 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:10:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a21107eb392ad352a11d88add9657687384931e5d889cdcf2e9933b4421077`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b0d166672182721ce571506f9d6ffbdf3978263c1e98a8c7cb83d70e5ceb3`  
		Last Modified: Tue, 09 Jun 2026 22:10:56 GMT  
		Size: 487.8 KB (487761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b460336fce54b4157c40e9e971fab0f408aeda838dde55bcf5ea5de52f3fa3`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea67caacc1b68dc837ec089a76c72de278a12c98986a9e7e27a6b4fa3f1f289`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9755d22906699b3ae49e1e7e643b80a71128ccb86715598896d101848d5074`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 20.0 MB (19967046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa89af8ddf8470a85bb4691fdf78f932741c527c8b8f25d9cdb0ab957b72766`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e31ea216b5955db20bf270de50921353f50fb244567aeffa9aec6a22bdf910`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0473ee7061cd54cff9f36e7d95856e8a0ad754f1afd89c20cff85132b100c5f`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d1bb31a8a58e6c19fa9476763d11417da6c9deccc5f3a25491e741f79611`  
		Last Modified: Tue, 09 Jun 2026 22:11:00 GMT  
		Size: 23.9 MB (23888859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e4bdf749ee7ad62af795111680dbce48097a254a3d53ebee0f0feb07f3820`  
		Last Modified: Tue, 09 Jun 2026 22:10:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdcd68b54960c0145901d3e97fbca29555cdd34359f1433932b88715f7ebd8a`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcecc97fe08a6e5f535dbb042a7e39cee7fd26ff6b8f64f4b87657d71a9ca42`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057fa34c824943d81b41f22bf794e23e40378d1db98addd0261c1fc64a152f55`  
		Last Modified: Tue, 09 Jun 2026 22:10:54 GMT  
		Size: 12.1 MB (12067581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9df2b61e3220bc07763d0d46ea3ea7d312e1e012d5c746cf9686ca44cd8b59cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `docker:29.5-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:e1874ace86696dc406093e614d34ce6a6f07ed7187e25f029685911a711ccc40
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188548521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d76e268d68e640ffd98a8af27bf187fba7876b6ac6253c294854ec499aed056`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:09:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:09:41 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:09:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:09 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:39 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:10:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a21107eb392ad352a11d88add9657687384931e5d889cdcf2e9933b4421077`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b0d166672182721ce571506f9d6ffbdf3978263c1e98a8c7cb83d70e5ceb3`  
		Last Modified: Tue, 09 Jun 2026 22:10:56 GMT  
		Size: 487.8 KB (487761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b460336fce54b4157c40e9e971fab0f408aeda838dde55bcf5ea5de52f3fa3`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea67caacc1b68dc837ec089a76c72de278a12c98986a9e7e27a6b4fa3f1f289`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9755d22906699b3ae49e1e7e643b80a71128ccb86715598896d101848d5074`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 20.0 MB (19967046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa89af8ddf8470a85bb4691fdf78f932741c527c8b8f25d9cdb0ab957b72766`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e31ea216b5955db20bf270de50921353f50fb244567aeffa9aec6a22bdf910`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0473ee7061cd54cff9f36e7d95856e8a0ad754f1afd89c20cff85132b100c5f`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d1bb31a8a58e6c19fa9476763d11417da6c9deccc5f3a25491e741f79611`  
		Last Modified: Tue, 09 Jun 2026 22:11:00 GMT  
		Size: 23.9 MB (23888859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e4bdf749ee7ad62af795111680dbce48097a254a3d53ebee0f0feb07f3820`  
		Last Modified: Tue, 09 Jun 2026 22:10:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdcd68b54960c0145901d3e97fbca29555cdd34359f1433932b88715f7ebd8a`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcecc97fe08a6e5f535dbb042a7e39cee7fd26ff6b8f64f4b87657d71a9ca42`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057fa34c824943d81b41f22bf794e23e40378d1db98addd0261c1fc64a152f55`  
		Last Modified: Tue, 09 Jun 2026 22:10:54 GMT  
		Size: 12.1 MB (12067581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b641303b79f48efd2803ac9c593cdd44c95c59202eb8d7e4380fa6caf293430b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `docker:29.5-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:626792a62ccf43d2c9c9f4106f25ac02fc10678a0f7ba40048484f76cccceb88
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335542989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9b36b1ba1723e3254afdfda83f60d48a67f885c462964ad4e4c9e14caea0a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:08:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:10:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:10:06 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:25 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:46 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:11:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e863137cc1a6c081981346b9911aa1b849767470cdb83cf8038b653b226e5`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13126202d74ea043ab743e8c58bf13f03d98c23877900c616afdb1fcb05ffc`  
		Last Modified: Tue, 09 Jun 2026 22:11:10 GMT  
		Size: 366.6 KB (366612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8450b716d93cc1abde208e2b7bbf780e835eedac6e83b3bf107dd22257e6d4f3`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0798499ee10239ba25cc04fb9b50137e1dc8535b2f0f7d8ec34d61a24e4334`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4335418e7b397c58162055ace3d049acef6d6a75695d40dcf7e1db5adcddc0e4`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 20.0 MB (20005460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82583ec76facc4e8c5d476866755314aac071c25b88ccc0714a9ea28cb9d5916`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c320c84b185908993c2ae455c8e19c447a3440d143e3df1e530688c2f2e48ab`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de253f20eb848fe03012cde3845923b7c3cbd8109b8848bcc65fe1a7e8ec78db`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1070177e1931be03c0bd9b077e590d23aba398d31e78f470b4a25895543ca9`  
		Last Modified: Tue, 09 Jun 2026 22:11:13 GMT  
		Size: 23.9 MB (23917170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44aca9e4206f912e275df50b300bb51b33594cb83228092fd0a1d7fda852d13`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09348bd8a2ac253880aff66aafdd100a7937ef94ecbd671ba62ea967a391c583`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0907212d8ad1bf4caaf2f7d9bae2ab4b6f11ce4bf246f2b3342a04b587941720`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d7087beffaf8878b9474aa75e2c3f844499000ed25a49af03ed7cf6ce3a487`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 12.1 MB (12099197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5.3`

```console
$ docker pull docker@sha256:7d85d0eda291f1a7ab6df4a9d1802b5ad4cf9145a088bd11188c78dcb5c7392b
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

### `docker:29.5.3` - linux; amd64

```console
$ docker pull docker@sha256:d175bec0f43b2aabf2f1cb375d3a0a5b540d60f82d3396dd473c835dea3525b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141571380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a47c98f97ef56a4b9ccfd268e6cc88eed4977222b3b66075165a05af9813e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3` - unknown; unknown

```console
$ docker pull docker@sha256:90d0717771cb46fea9e5335b4faf6b7fffffb29a8569967229f367338c4713c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0096914d04c0764856dcac037cc382383886bffdf3f73cbde86d3d89b5e25a`

```dockerfile
```

-	Layers:
	-	`sha256:8f74a25397fb78ec243dd8da45e2a676a6871587708f136f2b937886d980e124`  
		Last Modified: Thu, 04 Jun 2026 18:12:52 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:cccfdafc9b7735790124fc5ce0179ba190af4bfa1267ee56c21b069b0aa9b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133489319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3dd3e0f3eda4e49328697e623bcb5c2c4aa5a765ae25eb08fef63af492c8e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:49 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9698419a4fcfcfe53d39266385d0bdeadd8e3982c4c56be06088441af10d9d1a`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 7.3 MB (7278696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590d2829119f18520f97f8a0e744c191ca689d56c3945b532a37f4a1f57bf4f8`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 91.5 KB (91513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83f5308195cac080d9b65d0a2011263997412b414d259f7ad52d623c63a331`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd583d84ca571dbaf9008bdbaeae8371155aa2b4ead91c47494a7b421553b`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 64.0 MB (63954789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d3a29cd4fa1b4ca8c9a8bba57b6adec84495c4691cbf0a667f171ff9e49bd`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164bf1f4aad38e26ea7f523c0b8cd2508f1df7d8f39d65013f5e6b8a96ba3da`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3` - unknown; unknown

```console
$ docker pull docker@sha256:d1df1fb1e10855a2303e6295a1a17659f195d1845fc09ba6710eab2a82fa395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d89fb7855e5bc3e7e32727270386dd28a4f65936c4c472149c4c948063727`

```dockerfile
```

-	Layers:
	-	`sha256:81063e8f5ff0dc3d078be22a68c6973cfac7b866b95065c07c7597fff545894d`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:abd9432e46604318976d12dcb044b176e5a31ced7060b18602d42b54de200335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131594459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d33334019c68c6d9d380d7af58f0be8dbf0ae991cda104cd600dc29c2438e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3d7d1e69bcb16737aba3f84171773e55dc5e7293ab857fbbc754e0b61c181`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 6.6 MB (6577156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35895177edcf0459851a68da3f529aad815c6a06fc487bc78b67925822656c2`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 87.8 KB (87838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76012c6359cf96274f94e94ff4d395f8dcc9562130981ad47924978054b0f083`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a191244d67d45d9772df793ae4c4569cc18daab0aa247288428000db7a4e0a03`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 63.8 MB (63785660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0234b9f18f3e4e53673b485b84b67f0a658a88dc1de10bfe728995844996b`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad57512870cbfde869dda3537d23c6d1056b25b0243b1f2823b31e8771f9a2c`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3` - unknown; unknown

```console
$ docker pull docker@sha256:355b3babed5e09d804da8c33da9f3ed53746277aab8c1e43ecbe44c04cd09668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ccef25134c4f167d669bb33f7132a58a52e45c33d569d7679cdb81f001e0ff`

```dockerfile
```

-	Layers:
	-	`sha256:4eebc04a44848f48946a6c5a194b0c366123dae69712777b204e003616fecb18`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:387297c81bd1610b71e90a377ef6306f213d9262387b4d23883481a1f90a2550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130978501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ab87dbef3dcba50bd1de84ab87396a610d1281dba6f3e67f8ce5452fb2f67`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3` - unknown; unknown

```console
$ docker pull docker@sha256:d8a2f66d8cb21198f3c009790c921dd7f1940c10a3ad9d0235741829eb140e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7de24f830a299a1e537977495fbf842b9d31f3e70750c2f2ecd7c274283b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f227e53b9e53c71cc3a11d1d3c57f48e6fbdff69b2751016ea87727251e354e1`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5.3-alpine3.23`

```console
$ docker pull docker@sha256:7d85d0eda291f1a7ab6df4a9d1802b5ad4cf9145a088bd11188c78dcb5c7392b
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

### `docker:29.5.3-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:d175bec0f43b2aabf2f1cb375d3a0a5b540d60f82d3396dd473c835dea3525b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141571380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a47c98f97ef56a4b9ccfd268e6cc88eed4977222b3b66075165a05af9813e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:90d0717771cb46fea9e5335b4faf6b7fffffb29a8569967229f367338c4713c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0096914d04c0764856dcac037cc382383886bffdf3f73cbde86d3d89b5e25a`

```dockerfile
```

-	Layers:
	-	`sha256:8f74a25397fb78ec243dd8da45e2a676a6871587708f136f2b937886d980e124`  
		Last Modified: Thu, 04 Jun 2026 18:12:52 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:cccfdafc9b7735790124fc5ce0179ba190af4bfa1267ee56c21b069b0aa9b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133489319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3dd3e0f3eda4e49328697e623bcb5c2c4aa5a765ae25eb08fef63af492c8e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:49 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9698419a4fcfcfe53d39266385d0bdeadd8e3982c4c56be06088441af10d9d1a`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 7.3 MB (7278696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590d2829119f18520f97f8a0e744c191ca689d56c3945b532a37f4a1f57bf4f8`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 91.5 KB (91513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83f5308195cac080d9b65d0a2011263997412b414d259f7ad52d623c63a331`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd583d84ca571dbaf9008bdbaeae8371155aa2b4ead91c47494a7b421553b`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 64.0 MB (63954789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d3a29cd4fa1b4ca8c9a8bba57b6adec84495c4691cbf0a667f171ff9e49bd`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164bf1f4aad38e26ea7f523c0b8cd2508f1df7d8f39d65013f5e6b8a96ba3da`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:d1df1fb1e10855a2303e6295a1a17659f195d1845fc09ba6710eab2a82fa395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d89fb7855e5bc3e7e32727270386dd28a4f65936c4c472149c4c948063727`

```dockerfile
```

-	Layers:
	-	`sha256:81063e8f5ff0dc3d078be22a68c6973cfac7b866b95065c07c7597fff545894d`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:abd9432e46604318976d12dcb044b176e5a31ced7060b18602d42b54de200335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131594459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d33334019c68c6d9d380d7af58f0be8dbf0ae991cda104cd600dc29c2438e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3d7d1e69bcb16737aba3f84171773e55dc5e7293ab857fbbc754e0b61c181`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 6.6 MB (6577156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35895177edcf0459851a68da3f529aad815c6a06fc487bc78b67925822656c2`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 87.8 KB (87838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76012c6359cf96274f94e94ff4d395f8dcc9562130981ad47924978054b0f083`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a191244d67d45d9772df793ae4c4569cc18daab0aa247288428000db7a4e0a03`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 63.8 MB (63785660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0234b9f18f3e4e53673b485b84b67f0a658a88dc1de10bfe728995844996b`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad57512870cbfde869dda3537d23c6d1056b25b0243b1f2823b31e8771f9a2c`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:355b3babed5e09d804da8c33da9f3ed53746277aab8c1e43ecbe44c04cd09668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ccef25134c4f167d669bb33f7132a58a52e45c33d569d7679cdb81f001e0ff`

```dockerfile
```

-	Layers:
	-	`sha256:4eebc04a44848f48946a6c5a194b0c366123dae69712777b204e003616fecb18`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:387297c81bd1610b71e90a377ef6306f213d9262387b4d23883481a1f90a2550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130978501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ab87dbef3dcba50bd1de84ab87396a610d1281dba6f3e67f8ce5452fb2f67`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:d8a2f66d8cb21198f3c009790c921dd7f1940c10a3ad9d0235741829eb140e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7de24f830a299a1e537977495fbf842b9d31f3e70750c2f2ecd7c274283b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f227e53b9e53c71cc3a11d1d3c57f48e6fbdff69b2751016ea87727251e354e1`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5.3-cli`

```console
$ docker pull docker@sha256:873de13208aab9c1de73fe984fd45883e01464fcfcc85efa20aa56a9ccfe7aa6
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

### `docker:29.5.3-cli` - linux; amd64

```console
$ docker pull docker@sha256:d76a30ee8d7cc923cead6aef3e7b2b95ed8754dea7701f710d15e1fae1f70665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65862792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a00d98eb41b3144ec842f155d2688a13ed80d2fc5f1f70a8f73248d2e6f7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6923fa5011619a2d94dfb1d4ff853ff03adf7f2db967aa38854e8f4d47a067e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f22e60f4675b6e66a56713df1f73b70380a77fe284aaa7cf701b071382461f`

```dockerfile
```

-	Layers:
	-	`sha256:04ca03ce00ea392caae12cb4c437840b47f287abebf1d1dbf3a5bad2da881c8d`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:5bfff669277f7f9697c38c252600c46a60e34d6dcedbb6f23c1d37021555a2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62158321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ecff33f7643bd23d957b4136eff32e8ebac9add92b386c892caab32be32042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:383aab319724e2859039621d73e694f182f9804c673086928157477a580a8adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bc17dd1dec2758cdbc234dc801c256d93ec2ba6d3f5620c7dba50d7bf5943b`

```dockerfile
```

-	Layers:
	-	`sha256:e972de05273404ea4cc8d372a1b113a32138268f654e03e9a634ec9b338340c7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:902b3e5d8c1f3a8f50df537a2d569ec5369f96b8d7b47c4526a76e361f367297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61137803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927d1990201b745cb2b5c668aababaeac90c8053616f76665b152acf4c1d18ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d25246c6f6f19bc2d7bb5f113477aa78b540f39b79c54a54eed995e41fcd92b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a4d350556ced6cd5503c4b47b535e4f06598f7367f1a371a6050dec513a4c3`

```dockerfile
```

-	Layers:
	-	`sha256:974a2f1fef10826b93c3c467378744a0c7908059cc0c94c9493ead2bee490f37`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ed88538a7eb93cfa5e57b33d6544c182d423e7b55495f4f145896259bdbad899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61510517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a955ea7748f070ef6668ad2f79a466fa47e5ba52025c119d633d0be050605c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:566af4ebd5051b461ee31eba5e3e542993b993ea4553c8483383c2c5b38a7a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2462c1f7883cf00b4a0f6799aa4b5df7b02a32feacb94d8f8f4ce0969fc36d81`

```dockerfile
```

-	Layers:
	-	`sha256:d8cf46622fa8d5f46e8102daf4afbb68603f2bfd7a634800c67c95401a52a104`  
		Last Modified: Thu, 04 Jun 2026 18:07:58 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5.3-cli-alpine3.23`

```console
$ docker pull docker@sha256:873de13208aab9c1de73fe984fd45883e01464fcfcc85efa20aa56a9ccfe7aa6
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

### `docker:29.5.3-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:d76a30ee8d7cc923cead6aef3e7b2b95ed8754dea7701f710d15e1fae1f70665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65862792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a00d98eb41b3144ec842f155d2688a13ed80d2fc5f1f70a8f73248d2e6f7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:6923fa5011619a2d94dfb1d4ff853ff03adf7f2db967aa38854e8f4d47a067e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f22e60f4675b6e66a56713df1f73b70380a77fe284aaa7cf701b071382461f`

```dockerfile
```

-	Layers:
	-	`sha256:04ca03ce00ea392caae12cb4c437840b47f287abebf1d1dbf3a5bad2da881c8d`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:5bfff669277f7f9697c38c252600c46a60e34d6dcedbb6f23c1d37021555a2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62158321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ecff33f7643bd23d957b4136eff32e8ebac9add92b386c892caab32be32042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:383aab319724e2859039621d73e694f182f9804c673086928157477a580a8adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bc17dd1dec2758cdbc234dc801c256d93ec2ba6d3f5620c7dba50d7bf5943b`

```dockerfile
```

-	Layers:
	-	`sha256:e972de05273404ea4cc8d372a1b113a32138268f654e03e9a634ec9b338340c7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:902b3e5d8c1f3a8f50df537a2d569ec5369f96b8d7b47c4526a76e361f367297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61137803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927d1990201b745cb2b5c668aababaeac90c8053616f76665b152acf4c1d18ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:d25246c6f6f19bc2d7bb5f113477aa78b540f39b79c54a54eed995e41fcd92b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a4d350556ced6cd5503c4b47b535e4f06598f7367f1a371a6050dec513a4c3`

```dockerfile
```

-	Layers:
	-	`sha256:974a2f1fef10826b93c3c467378744a0c7908059cc0c94c9493ead2bee490f37`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ed88538a7eb93cfa5e57b33d6544c182d423e7b55495f4f145896259bdbad899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61510517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a955ea7748f070ef6668ad2f79a466fa47e5ba52025c119d633d0be050605c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:566af4ebd5051b461ee31eba5e3e542993b993ea4553c8483383c2c5b38a7a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2462c1f7883cf00b4a0f6799aa4b5df7b02a32feacb94d8f8f4ce0969fc36d81`

```dockerfile
```

-	Layers:
	-	`sha256:d8cf46622fa8d5f46e8102daf4afbb68603f2bfd7a634800c67c95401a52a104`  
		Last Modified: Thu, 04 Jun 2026 18:07:58 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5.3-dind`

```console
$ docker pull docker@sha256:7d85d0eda291f1a7ab6df4a9d1802b5ad4cf9145a088bd11188c78dcb5c7392b
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

### `docker:29.5.3-dind` - linux; amd64

```console
$ docker pull docker@sha256:d175bec0f43b2aabf2f1cb375d3a0a5b540d60f82d3396dd473c835dea3525b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141571380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a47c98f97ef56a4b9ccfd268e6cc88eed4977222b3b66075165a05af9813e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:90d0717771cb46fea9e5335b4faf6b7fffffb29a8569967229f367338c4713c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0096914d04c0764856dcac037cc382383886bffdf3f73cbde86d3d89b5e25a`

```dockerfile
```

-	Layers:
	-	`sha256:8f74a25397fb78ec243dd8da45e2a676a6871587708f136f2b937886d980e124`  
		Last Modified: Thu, 04 Jun 2026 18:12:52 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:cccfdafc9b7735790124fc5ce0179ba190af4bfa1267ee56c21b069b0aa9b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133489319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3dd3e0f3eda4e49328697e623bcb5c2c4aa5a765ae25eb08fef63af492c8e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:49 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9698419a4fcfcfe53d39266385d0bdeadd8e3982c4c56be06088441af10d9d1a`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 7.3 MB (7278696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590d2829119f18520f97f8a0e744c191ca689d56c3945b532a37f4a1f57bf4f8`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 91.5 KB (91513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83f5308195cac080d9b65d0a2011263997412b414d259f7ad52d623c63a331`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd583d84ca571dbaf9008bdbaeae8371155aa2b4ead91c47494a7b421553b`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 64.0 MB (63954789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d3a29cd4fa1b4ca8c9a8bba57b6adec84495c4691cbf0a667f171ff9e49bd`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164bf1f4aad38e26ea7f523c0b8cd2508f1df7d8f39d65013f5e6b8a96ba3da`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d1df1fb1e10855a2303e6295a1a17659f195d1845fc09ba6710eab2a82fa395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d89fb7855e5bc3e7e32727270386dd28a4f65936c4c472149c4c948063727`

```dockerfile
```

-	Layers:
	-	`sha256:81063e8f5ff0dc3d078be22a68c6973cfac7b866b95065c07c7597fff545894d`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:abd9432e46604318976d12dcb044b176e5a31ced7060b18602d42b54de200335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131594459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d33334019c68c6d9d380d7af58f0be8dbf0ae991cda104cd600dc29c2438e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3d7d1e69bcb16737aba3f84171773e55dc5e7293ab857fbbc754e0b61c181`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 6.6 MB (6577156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35895177edcf0459851a68da3f529aad815c6a06fc487bc78b67925822656c2`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 87.8 KB (87838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76012c6359cf96274f94e94ff4d395f8dcc9562130981ad47924978054b0f083`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a191244d67d45d9772df793ae4c4569cc18daab0aa247288428000db7a4e0a03`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 63.8 MB (63785660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0234b9f18f3e4e53673b485b84b67f0a658a88dc1de10bfe728995844996b`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad57512870cbfde869dda3537d23c6d1056b25b0243b1f2823b31e8771f9a2c`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:355b3babed5e09d804da8c33da9f3ed53746277aab8c1e43ecbe44c04cd09668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ccef25134c4f167d669bb33f7132a58a52e45c33d569d7679cdb81f001e0ff`

```dockerfile
```

-	Layers:
	-	`sha256:4eebc04a44848f48946a6c5a194b0c366123dae69712777b204e003616fecb18`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:387297c81bd1610b71e90a377ef6306f213d9262387b4d23883481a1f90a2550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130978501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ab87dbef3dcba50bd1de84ab87396a610d1281dba6f3e67f8ce5452fb2f67`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d8a2f66d8cb21198f3c009790c921dd7f1940c10a3ad9d0235741829eb140e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7de24f830a299a1e537977495fbf842b9d31f3e70750c2f2ecd7c274283b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f227e53b9e53c71cc3a11d1d3c57f48e6fbdff69b2751016ea87727251e354e1`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5.3-dind-alpine3.23`

```console
$ docker pull docker@sha256:7d85d0eda291f1a7ab6df4a9d1802b5ad4cf9145a088bd11188c78dcb5c7392b
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

### `docker:29.5.3-dind-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:d175bec0f43b2aabf2f1cb375d3a0a5b540d60f82d3396dd473c835dea3525b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141571380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a47c98f97ef56a4b9ccfd268e6cc88eed4977222b3b66075165a05af9813e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:90d0717771cb46fea9e5335b4faf6b7fffffb29a8569967229f367338c4713c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0096914d04c0764856dcac037cc382383886bffdf3f73cbde86d3d89b5e25a`

```dockerfile
```

-	Layers:
	-	`sha256:8f74a25397fb78ec243dd8da45e2a676a6871587708f136f2b937886d980e124`  
		Last Modified: Thu, 04 Jun 2026 18:12:52 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-dind-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:cccfdafc9b7735790124fc5ce0179ba190af4bfa1267ee56c21b069b0aa9b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133489319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3dd3e0f3eda4e49328697e623bcb5c2c4aa5a765ae25eb08fef63af492c8e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:49 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9698419a4fcfcfe53d39266385d0bdeadd8e3982c4c56be06088441af10d9d1a`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 7.3 MB (7278696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590d2829119f18520f97f8a0e744c191ca689d56c3945b532a37f4a1f57bf4f8`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 91.5 KB (91513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83f5308195cac080d9b65d0a2011263997412b414d259f7ad52d623c63a331`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd583d84ca571dbaf9008bdbaeae8371155aa2b4ead91c47494a7b421553b`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 64.0 MB (63954789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d3a29cd4fa1b4ca8c9a8bba57b6adec84495c4691cbf0a667f171ff9e49bd`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164bf1f4aad38e26ea7f523c0b8cd2508f1df7d8f39d65013f5e6b8a96ba3da`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:d1df1fb1e10855a2303e6295a1a17659f195d1845fc09ba6710eab2a82fa395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d89fb7855e5bc3e7e32727270386dd28a4f65936c4c472149c4c948063727`

```dockerfile
```

-	Layers:
	-	`sha256:81063e8f5ff0dc3d078be22a68c6973cfac7b866b95065c07c7597fff545894d`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-dind-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:abd9432e46604318976d12dcb044b176e5a31ced7060b18602d42b54de200335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131594459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d33334019c68c6d9d380d7af58f0be8dbf0ae991cda104cd600dc29c2438e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3d7d1e69bcb16737aba3f84171773e55dc5e7293ab857fbbc754e0b61c181`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 6.6 MB (6577156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35895177edcf0459851a68da3f529aad815c6a06fc487bc78b67925822656c2`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 87.8 KB (87838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76012c6359cf96274f94e94ff4d395f8dcc9562130981ad47924978054b0f083`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a191244d67d45d9772df793ae4c4569cc18daab0aa247288428000db7a4e0a03`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 63.8 MB (63785660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0234b9f18f3e4e53673b485b84b67f0a658a88dc1de10bfe728995844996b`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad57512870cbfde869dda3537d23c6d1056b25b0243b1f2823b31e8771f9a2c`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:355b3babed5e09d804da8c33da9f3ed53746277aab8c1e43ecbe44c04cd09668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ccef25134c4f167d669bb33f7132a58a52e45c33d569d7679cdb81f001e0ff`

```dockerfile
```

-	Layers:
	-	`sha256:4eebc04a44848f48946a6c5a194b0c366123dae69712777b204e003616fecb18`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-dind-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:387297c81bd1610b71e90a377ef6306f213d9262387b4d23883481a1f90a2550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130978501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ab87dbef3dcba50bd1de84ab87396a610d1281dba6f3e67f8ce5452fb2f67`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:d8a2f66d8cb21198f3c009790c921dd7f1940c10a3ad9d0235741829eb140e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7de24f830a299a1e537977495fbf842b9d31f3e70750c2f2ecd7c274283b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f227e53b9e53c71cc3a11d1d3c57f48e6fbdff69b2751016ea87727251e354e1`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5.3-dind-rootless`

```console
$ docker pull docker@sha256:41825fb12da6b78219af4b862830f252be1f5dee3d6cbfd508736ed31c0014d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.5.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9f5c3cc894bf49af0667c5b2662b9a4f309d079aa0337324bdca7b748e964876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157096105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b737c7bee606e4bc72ac59c92d9b4d8dd1d2dc020ac6619938ab8d25579309e4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
# Thu, 04 Jun 2026 18:14:30 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Jun 2026 18:14:30 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Jun 2026 18:14:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Jun 2026 18:14:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2db229f6b5fa1fd732d8fba1e949c5c7e73e730e16357c16495923eb4de021c`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 3.4 MB (3420079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bd807b36584452264c40c10ca5b43c04108f21f4a61575c208ad0f6fcea4c3`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d4aff48ac38b7051cfccbdaced29f5b735a83a9f6387ccfe30cc5fd7b83084`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8974b16bb9e50c8552367b5aba959a7bdd24079a8b84430486638e82c3c02ff`  
		Last Modified: Thu, 04 Jun 2026 18:14:37 GMT  
		Size: 12.1 MB (12103307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad90cb2bc6565f2bfe4570ff4400df96b165f0c295dfae388f2b502aaf504ec`  
		Last Modified: Thu, 04 Jun 2026 18:14:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:210086fd9e446a787d03d83b9f6d28e95bd05fc7b752495c6ad1b684e7a5107f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239d1603cd7d20cf2b717faedf8a6799cb79831f582f00904a69213db49adb`

```dockerfile
```

-	Layers:
	-	`sha256:3605fd3d07b5c864bed987b1cf0900c688cb6b5a4886cd6e9eaf96384171485c`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 30.5 KB (30492 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b61013cc22712072617daa3684a4b51259ee5b5b9a5e1cb31958ebda52b6a697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145611456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46aee58794f1f1bb31fcc972c975b297b4970c7f6b648186ff66800511ed2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
# Thu, 04 Jun 2026 18:14:37 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Jun 2026 18:14:37 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e24e15f563ca4ef38267a4ece0cde7eb2ea2b6c71439f2f8ad3e681bf0dc8c`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 3.4 MB (3394532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd56f3c1721d727b2bb80a572d12001a4da9f269d19ca40ba68f13201572e54`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98aaab4cf1e555e08f7d5aac3445aab4317f29393ae87857469d74d15e942de`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938547d0fb3967e62653e6b2649c8dfc048576f66f32576f7432a81466be2fcb`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 11.2 MB (11237084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d35d5c447eb8a4e37a5670c1c0b25137c3d27f3bd6a58b34de7f8df41959c2`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c2743e70adcc0e287ee4767cc6b01965cd3e1298f2f2b97bb5583213e323bff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d7ef8ce3af550022eb687e4d68f22fcb3f28226bd5c9c481cccba58d5ad5ad`

```dockerfile
```

-	Layers:
	-	`sha256:dd88782a3b7d95075d0232118200d547b991e9eb5674d30ca0febba0efc0cafe`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5.3-windowsservercore`

```console
$ docker pull docker@sha256:a4506ea88c29d83e0c6f74a20dde3d510d490377feb330023763fc4180ede82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `docker:29.5.3-windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:626792a62ccf43d2c9c9f4106f25ac02fc10678a0f7ba40048484f76cccceb88
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335542989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9b36b1ba1723e3254afdfda83f60d48a67f885c462964ad4e4c9e14caea0a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:08:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:10:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:10:06 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:25 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:46 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:11:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e863137cc1a6c081981346b9911aa1b849767470cdb83cf8038b653b226e5`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13126202d74ea043ab743e8c58bf13f03d98c23877900c616afdb1fcb05ffc`  
		Last Modified: Tue, 09 Jun 2026 22:11:10 GMT  
		Size: 366.6 KB (366612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8450b716d93cc1abde208e2b7bbf780e835eedac6e83b3bf107dd22257e6d4f3`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0798499ee10239ba25cc04fb9b50137e1dc8535b2f0f7d8ec34d61a24e4334`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4335418e7b397c58162055ace3d049acef6d6a75695d40dcf7e1db5adcddc0e4`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 20.0 MB (20005460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82583ec76facc4e8c5d476866755314aac071c25b88ccc0714a9ea28cb9d5916`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c320c84b185908993c2ae455c8e19c447a3440d143e3df1e530688c2f2e48ab`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de253f20eb848fe03012cde3845923b7c3cbd8109b8848bcc65fe1a7e8ec78db`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1070177e1931be03c0bd9b077e590d23aba398d31e78f470b4a25895543ca9`  
		Last Modified: Tue, 09 Jun 2026 22:11:13 GMT  
		Size: 23.9 MB (23917170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44aca9e4206f912e275df50b300bb51b33594cb83228092fd0a1d7fda852d13`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09348bd8a2ac253880aff66aafdd100a7937ef94ecbd671ba62ea967a391c583`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0907212d8ad1bf4caaf2f7d9bae2ab4b6f11ce4bf246f2b3342a04b587941720`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d7087beffaf8878b9474aa75e2c3f844499000ed25a49af03ed7cf6ce3a487`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 12.1 MB (12099197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.5.3-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:e1874ace86696dc406093e614d34ce6a6f07ed7187e25f029685911a711ccc40
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188548521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d76e268d68e640ffd98a8af27bf187fba7876b6ac6253c294854ec499aed056`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:09:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:09:41 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:09:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:09 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:39 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:10:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a21107eb392ad352a11d88add9657687384931e5d889cdcf2e9933b4421077`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b0d166672182721ce571506f9d6ffbdf3978263c1e98a8c7cb83d70e5ceb3`  
		Last Modified: Tue, 09 Jun 2026 22:10:56 GMT  
		Size: 487.8 KB (487761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b460336fce54b4157c40e9e971fab0f408aeda838dde55bcf5ea5de52f3fa3`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea67caacc1b68dc837ec089a76c72de278a12c98986a9e7e27a6b4fa3f1f289`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9755d22906699b3ae49e1e7e643b80a71128ccb86715598896d101848d5074`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 20.0 MB (19967046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa89af8ddf8470a85bb4691fdf78f932741c527c8b8f25d9cdb0ab957b72766`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e31ea216b5955db20bf270de50921353f50fb244567aeffa9aec6a22bdf910`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0473ee7061cd54cff9f36e7d95856e8a0ad754f1afd89c20cff85132b100c5f`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d1bb31a8a58e6c19fa9476763d11417da6c9deccc5f3a25491e741f79611`  
		Last Modified: Tue, 09 Jun 2026 22:11:00 GMT  
		Size: 23.9 MB (23888859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e4bdf749ee7ad62af795111680dbce48097a254a3d53ebee0f0feb07f3820`  
		Last Modified: Tue, 09 Jun 2026 22:10:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdcd68b54960c0145901d3e97fbca29555cdd34359f1433932b88715f7ebd8a`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcecc97fe08a6e5f535dbb042a7e39cee7fd26ff6b8f64f4b87657d71a9ca42`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057fa34c824943d81b41f22bf794e23e40378d1db98addd0261c1fc64a152f55`  
		Last Modified: Tue, 09 Jun 2026 22:10:54 GMT  
		Size: 12.1 MB (12067581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9df2b61e3220bc07763d0d46ea3ea7d312e1e012d5c746cf9686ca44cd8b59cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `docker:29.5.3-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:e1874ace86696dc406093e614d34ce6a6f07ed7187e25f029685911a711ccc40
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188548521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d76e268d68e640ffd98a8af27bf187fba7876b6ac6253c294854ec499aed056`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:09:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:09:41 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:09:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:09 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:39 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:10:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a21107eb392ad352a11d88add9657687384931e5d889cdcf2e9933b4421077`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b0d166672182721ce571506f9d6ffbdf3978263c1e98a8c7cb83d70e5ceb3`  
		Last Modified: Tue, 09 Jun 2026 22:10:56 GMT  
		Size: 487.8 KB (487761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b460336fce54b4157c40e9e971fab0f408aeda838dde55bcf5ea5de52f3fa3`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea67caacc1b68dc837ec089a76c72de278a12c98986a9e7e27a6b4fa3f1f289`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9755d22906699b3ae49e1e7e643b80a71128ccb86715598896d101848d5074`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 20.0 MB (19967046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa89af8ddf8470a85bb4691fdf78f932741c527c8b8f25d9cdb0ab957b72766`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e31ea216b5955db20bf270de50921353f50fb244567aeffa9aec6a22bdf910`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0473ee7061cd54cff9f36e7d95856e8a0ad754f1afd89c20cff85132b100c5f`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d1bb31a8a58e6c19fa9476763d11417da6c9deccc5f3a25491e741f79611`  
		Last Modified: Tue, 09 Jun 2026 22:11:00 GMT  
		Size: 23.9 MB (23888859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e4bdf749ee7ad62af795111680dbce48097a254a3d53ebee0f0feb07f3820`  
		Last Modified: Tue, 09 Jun 2026 22:10:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdcd68b54960c0145901d3e97fbca29555cdd34359f1433932b88715f7ebd8a`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcecc97fe08a6e5f535dbb042a7e39cee7fd26ff6b8f64f4b87657d71a9ca42`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057fa34c824943d81b41f22bf794e23e40378d1db98addd0261c1fc64a152f55`  
		Last Modified: Tue, 09 Jun 2026 22:10:54 GMT  
		Size: 12.1 MB (12067581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5.3-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b641303b79f48efd2803ac9c593cdd44c95c59202eb8d7e4380fa6caf293430b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `docker:29.5.3-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:626792a62ccf43d2c9c9f4106f25ac02fc10678a0f7ba40048484f76cccceb88
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335542989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9b36b1ba1723e3254afdfda83f60d48a67f885c462964ad4e4c9e14caea0a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:08:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:10:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:10:06 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:25 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:46 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:11:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e863137cc1a6c081981346b9911aa1b849767470cdb83cf8038b653b226e5`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13126202d74ea043ab743e8c58bf13f03d98c23877900c616afdb1fcb05ffc`  
		Last Modified: Tue, 09 Jun 2026 22:11:10 GMT  
		Size: 366.6 KB (366612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8450b716d93cc1abde208e2b7bbf780e835eedac6e83b3bf107dd22257e6d4f3`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0798499ee10239ba25cc04fb9b50137e1dc8535b2f0f7d8ec34d61a24e4334`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4335418e7b397c58162055ace3d049acef6d6a75695d40dcf7e1db5adcddc0e4`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 20.0 MB (20005460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82583ec76facc4e8c5d476866755314aac071c25b88ccc0714a9ea28cb9d5916`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c320c84b185908993c2ae455c8e19c447a3440d143e3df1e530688c2f2e48ab`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de253f20eb848fe03012cde3845923b7c3cbd8109b8848bcc65fe1a7e8ec78db`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1070177e1931be03c0bd9b077e590d23aba398d31e78f470b4a25895543ca9`  
		Last Modified: Tue, 09 Jun 2026 22:11:13 GMT  
		Size: 23.9 MB (23917170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44aca9e4206f912e275df50b300bb51b33594cb83228092fd0a1d7fda852d13`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09348bd8a2ac253880aff66aafdd100a7937ef94ecbd671ba62ea967a391c583`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0907212d8ad1bf4caaf2f7d9bae2ab4b6f11ce4bf246f2b3342a04b587941720`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d7087beffaf8878b9474aa75e2c3f844499000ed25a49af03ed7cf6ce3a487`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 12.1 MB (12099197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:873de13208aab9c1de73fe984fd45883e01464fcfcc85efa20aa56a9ccfe7aa6
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
$ docker pull docker@sha256:d76a30ee8d7cc923cead6aef3e7b2b95ed8754dea7701f710d15e1fae1f70665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65862792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a00d98eb41b3144ec842f155d2688a13ed80d2fc5f1f70a8f73248d2e6f7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6923fa5011619a2d94dfb1d4ff853ff03adf7f2db967aa38854e8f4d47a067e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f22e60f4675b6e66a56713df1f73b70380a77fe284aaa7cf701b071382461f`

```dockerfile
```

-	Layers:
	-	`sha256:04ca03ce00ea392caae12cb4c437840b47f287abebf1d1dbf3a5bad2da881c8d`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:5bfff669277f7f9697c38c252600c46a60e34d6dcedbb6f23c1d37021555a2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62158321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ecff33f7643bd23d957b4136eff32e8ebac9add92b386c892caab32be32042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:383aab319724e2859039621d73e694f182f9804c673086928157477a580a8adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bc17dd1dec2758cdbc234dc801c256d93ec2ba6d3f5620c7dba50d7bf5943b`

```dockerfile
```

-	Layers:
	-	`sha256:e972de05273404ea4cc8d372a1b113a32138268f654e03e9a634ec9b338340c7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:902b3e5d8c1f3a8f50df537a2d569ec5369f96b8d7b47c4526a76e361f367297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61137803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927d1990201b745cb2b5c668aababaeac90c8053616f76665b152acf4c1d18ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:d25246c6f6f19bc2d7bb5f113477aa78b540f39b79c54a54eed995e41fcd92b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a4d350556ced6cd5503c4b47b535e4f06598f7367f1a371a6050dec513a4c3`

```dockerfile
```

-	Layers:
	-	`sha256:974a2f1fef10826b93c3c467378744a0c7908059cc0c94c9493ead2bee490f37`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ed88538a7eb93cfa5e57b33d6544c182d423e7b55495f4f145896259bdbad899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61510517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a955ea7748f070ef6668ad2f79a466fa47e5ba52025c119d633d0be050605c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:566af4ebd5051b461ee31eba5e3e542993b993ea4553c8483383c2c5b38a7a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2462c1f7883cf00b4a0f6799aa4b5df7b02a32feacb94d8f8f4ce0969fc36d81`

```dockerfile
```

-	Layers:
	-	`sha256:d8cf46622fa8d5f46e8102daf4afbb68603f2bfd7a634800c67c95401a52a104`  
		Last Modified: Thu, 04 Jun 2026 18:07:58 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:7d85d0eda291f1a7ab6df4a9d1802b5ad4cf9145a088bd11188c78dcb5c7392b
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
$ docker pull docker@sha256:d175bec0f43b2aabf2f1cb375d3a0a5b540d60f82d3396dd473c835dea3525b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141571380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a47c98f97ef56a4b9ccfd268e6cc88eed4977222b3b66075165a05af9813e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:90d0717771cb46fea9e5335b4faf6b7fffffb29a8569967229f367338c4713c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0096914d04c0764856dcac037cc382383886bffdf3f73cbde86d3d89b5e25a`

```dockerfile
```

-	Layers:
	-	`sha256:8f74a25397fb78ec243dd8da45e2a676a6871587708f136f2b937886d980e124`  
		Last Modified: Thu, 04 Jun 2026 18:12:52 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:cccfdafc9b7735790124fc5ce0179ba190af4bfa1267ee56c21b069b0aa9b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133489319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3dd3e0f3eda4e49328697e623bcb5c2c4aa5a765ae25eb08fef63af492c8e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:49 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9698419a4fcfcfe53d39266385d0bdeadd8e3982c4c56be06088441af10d9d1a`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 7.3 MB (7278696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590d2829119f18520f97f8a0e744c191ca689d56c3945b532a37f4a1f57bf4f8`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 91.5 KB (91513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83f5308195cac080d9b65d0a2011263997412b414d259f7ad52d623c63a331`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd583d84ca571dbaf9008bdbaeae8371155aa2b4ead91c47494a7b421553b`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 64.0 MB (63954789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d3a29cd4fa1b4ca8c9a8bba57b6adec84495c4691cbf0a667f171ff9e49bd`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164bf1f4aad38e26ea7f523c0b8cd2508f1df7d8f39d65013f5e6b8a96ba3da`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:d1df1fb1e10855a2303e6295a1a17659f195d1845fc09ba6710eab2a82fa395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d89fb7855e5bc3e7e32727270386dd28a4f65936c4c472149c4c948063727`

```dockerfile
```

-	Layers:
	-	`sha256:81063e8f5ff0dc3d078be22a68c6973cfac7b866b95065c07c7597fff545894d`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:abd9432e46604318976d12dcb044b176e5a31ced7060b18602d42b54de200335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131594459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d33334019c68c6d9d380d7af58f0be8dbf0ae991cda104cd600dc29c2438e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3d7d1e69bcb16737aba3f84171773e55dc5e7293ab857fbbc754e0b61c181`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 6.6 MB (6577156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35895177edcf0459851a68da3f529aad815c6a06fc487bc78b67925822656c2`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 87.8 KB (87838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76012c6359cf96274f94e94ff4d395f8dcc9562130981ad47924978054b0f083`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a191244d67d45d9772df793ae4c4569cc18daab0aa247288428000db7a4e0a03`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 63.8 MB (63785660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0234b9f18f3e4e53673b485b84b67f0a658a88dc1de10bfe728995844996b`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad57512870cbfde869dda3537d23c6d1056b25b0243b1f2823b31e8771f9a2c`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:355b3babed5e09d804da8c33da9f3ed53746277aab8c1e43ecbe44c04cd09668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ccef25134c4f167d669bb33f7132a58a52e45c33d569d7679cdb81f001e0ff`

```dockerfile
```

-	Layers:
	-	`sha256:4eebc04a44848f48946a6c5a194b0c366123dae69712777b204e003616fecb18`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:387297c81bd1610b71e90a377ef6306f213d9262387b4d23883481a1f90a2550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130978501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ab87dbef3dcba50bd1de84ab87396a610d1281dba6f3e67f8ce5452fb2f67`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:d8a2f66d8cb21198f3c009790c921dd7f1940c10a3ad9d0235741829eb140e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7de24f830a299a1e537977495fbf842b9d31f3e70750c2f2ecd7c274283b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f227e53b9e53c71cc3a11d1d3c57f48e6fbdff69b2751016ea87727251e354e1`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:41825fb12da6b78219af4b862830f252be1f5dee3d6cbfd508736ed31c0014d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9f5c3cc894bf49af0667c5b2662b9a4f309d079aa0337324bdca7b748e964876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157096105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b737c7bee606e4bc72ac59c92d9b4d8dd1d2dc020ac6619938ab8d25579309e4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
# Thu, 04 Jun 2026 18:14:30 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Jun 2026 18:14:30 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Jun 2026 18:14:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Jun 2026 18:14:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Jun 2026 18:14:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2db229f6b5fa1fd732d8fba1e949c5c7e73e730e16357c16495923eb4de021c`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 3.4 MB (3420079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bd807b36584452264c40c10ca5b43c04108f21f4a61575c208ad0f6fcea4c3`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d4aff48ac38b7051cfccbdaced29f5b735a83a9f6387ccfe30cc5fd7b83084`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8974b16bb9e50c8552367b5aba959a7bdd24079a8b84430486638e82c3c02ff`  
		Last Modified: Thu, 04 Jun 2026 18:14:37 GMT  
		Size: 12.1 MB (12103307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad90cb2bc6565f2bfe4570ff4400df96b165f0c295dfae388f2b502aaf504ec`  
		Last Modified: Thu, 04 Jun 2026 18:14:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:210086fd9e446a787d03d83b9f6d28e95bd05fc7b752495c6ad1b684e7a5107f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239d1603cd7d20cf2b717faedf8a6799cb79831f582f00904a69213db49adb`

```dockerfile
```

-	Layers:
	-	`sha256:3605fd3d07b5c864bed987b1cf0900c688cb6b5a4886cd6e9eaf96384171485c`  
		Last Modified: Thu, 04 Jun 2026 18:14:36 GMT  
		Size: 30.5 KB (30492 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b61013cc22712072617daa3684a4b51259ee5b5b9a5e1cb31958ebda52b6a697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145611456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46aee58794f1f1bb31fcc972c975b297b4970c7f6b648186ff66800511ed2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
# Thu, 04 Jun 2026 18:14:37 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Jun 2026 18:14:37 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Jun 2026 18:14:37 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e24e15f563ca4ef38267a4ece0cde7eb2ea2b6c71439f2f8ad3e681bf0dc8c`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 3.4 MB (3394532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd56f3c1721d727b2bb80a572d12001a4da9f269d19ca40ba68f13201572e54`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98aaab4cf1e555e08f7d5aac3445aab4317f29393ae87857469d74d15e942de`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938547d0fb3967e62653e6b2649c8dfc048576f66f32576f7432a81466be2fcb`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 11.2 MB (11237084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d35d5c447eb8a4e37a5670c1c0b25137c3d27f3bd6a58b34de7f8df41959c2`  
		Last Modified: Thu, 04 Jun 2026 18:14:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c2743e70adcc0e287ee4767cc6b01965cd3e1298f2f2b97bb5583213e323bff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d7ef8ce3af550022eb687e4d68f22fcb3f28226bd5c9c481cccba58d5ad5ad`

```dockerfile
```

-	Layers:
	-	`sha256:dd88782a3b7d95075d0232118200d547b991e9eb5674d30ca0febba0efc0cafe`  
		Last Modified: Thu, 04 Jun 2026 18:14:42 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:7d85d0eda291f1a7ab6df4a9d1802b5ad4cf9145a088bd11188c78dcb5c7392b
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
$ docker pull docker@sha256:d175bec0f43b2aabf2f1cb375d3a0a5b540d60f82d3396dd473c835dea3525b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141571380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a47c98f97ef56a4b9ccfd268e6cc88eed4977222b3b66075165a05af9813e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:07 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:42 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420aebb57fdec7b93c28f1059f3d08b6eee2a8efea16ba604d779f9e9afa0b`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 8.3 MB (8311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93b2e4d135ab5f4e1310d5814b0e654cd2f2701543483eec5465ae25c220db`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1222cc31827ff135bb3f89950707fb05e67545b0ae91b8b8bd78db656831c2`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 19.3 MB (19300003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4117cbbb76ab361bbe5058f8b426471a8cda04eaa4bf6dd7ad175ff2a33d61`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbdc46dae7eaa2efc2ec682a52532be28cad0d71fcb1b238e31541b5b53bd1`  
		Last Modified: Thu, 04 Jun 2026 18:08:15 GMT  
		Size: 11.4 MB (11395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076a2f420cbe08a25f14a75d3e6b227145f51e1e509cee608885d3a4949252d`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12895266f01ae00a20cb256de03e6e572904b00a680f1d0617eba62215d13e`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887d264b256463be05a1c0f163005ff06581deeeacfa52e0a9b54efb9c38d0`  
		Last Modified: Thu, 04 Jun 2026 18:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e2fce8ed14f8ddca858382b8454294692e66a093d14d1228002e10a916a71`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 6.9 MB (6941416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d523243d9e7c38eb4529602edc09f458572c13294c18582642ce34ee7342dee`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 92.2 KB (92216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c2b46154e45c8e24fcbd07be5c86ed8cee0c9ead557bb6bee4a9fe171ed29`  
		Last Modified: Thu, 04 Jun 2026 18:12:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc28bcc785088d0cc956a4baf774bc2285515f95e966479cc5818df6d25c6b5`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 68.7 MB (68668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff9d865943c0fa6cd22ceee1df658ce38dc70aa2a29ef1dfcb2eab16729332`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc44203174003d0699a9579430c8e9b8bd5ac27b6b5be2f6dbfdb0833fd79`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:90d0717771cb46fea9e5335b4faf6b7fffffb29a8569967229f367338c4713c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0096914d04c0764856dcac037cc382383886bffdf3f73cbde86d3d89b5e25a`

```dockerfile
```

-	Layers:
	-	`sha256:8f74a25397fb78ec243dd8da45e2a676a6871587708f136f2b937886d980e124`  
		Last Modified: Thu, 04 Jun 2026 18:12:52 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:cccfdafc9b7735790124fc5ce0179ba190af4bfa1267ee56c21b069b0aa9b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133489319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3dd3e0f3eda4e49328697e623bcb5c2c4aa5a765ae25eb08fef63af492c8e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:43 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:49 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47223fd288cfa74709e1d26e3f8b0c76e5849ee154b5781a99e40712573708d8`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 8.2 MB (8211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11cfd36aa0314105cda1c05abfdcc8424defb27459a0f7902211b0c22e0a3d7`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32e9e36c1f44c910af8dce906e8d207918c4efd8047a381eb69c68737c4259`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 17.9 MB (17945236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aaa34371384585b73902cd58b1ed3a8bab6161e1897825118a78719b9ae6cd`  
		Last Modified: Thu, 04 Jun 2026 18:07:50 GMT  
		Size: 21.6 MB (21614620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ca6f5adc72d7d4e6712608f3543229e5d8c3db8541dd05fb22216e9995b29`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 10.8 MB (10812569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c6700329baa2c96d0a9cdc535b8f4d20a373a15b4041744f9f7bed4c8da3a`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a987d4513b347a4e93172238735248fff53c6eb0163a99dc02b0e38dd02c0`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe16a63e959c61d286687c7d44f50364010480cb9ca7ce0e5c12babd460d8fa`  
		Last Modified: Thu, 04 Jun 2026 18:07:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9698419a4fcfcfe53d39266385d0bdeadd8e3982c4c56be06088441af10d9d1a`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 7.3 MB (7278696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590d2829119f18520f97f8a0e744c191ca689d56c3945b532a37f4a1f57bf4f8`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 91.5 KB (91513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83f5308195cac080d9b65d0a2011263997412b414d259f7ad52d623c63a331`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd583d84ca571dbaf9008bdbaeae8371155aa2b4ead91c47494a7b421553b`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 64.0 MB (63954789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d3a29cd4fa1b4ca8c9a8bba57b6adec84495c4691cbf0a667f171ff9e49bd`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164bf1f4aad38e26ea7f523c0b8cd2508f1df7d8f39d65013f5e6b8a96ba3da`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:d1df1fb1e10855a2303e6295a1a17659f195d1845fc09ba6710eab2a82fa395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d89fb7855e5bc3e7e32727270386dd28a4f65936c4c472149c4c948063727`

```dockerfile
```

-	Layers:
	-	`sha256:81063e8f5ff0dc3d078be22a68c6973cfac7b866b95065c07c7597fff545894d`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:abd9432e46604318976d12dcb044b176e5a31ced7060b18602d42b54de200335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131594459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d33334019c68c6d9d380d7af58f0be8dbf0ae991cda104cd600dc29c2438e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:08:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:08:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:08:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:08:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:08:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:08:49 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d5cecbd32cccf66bcca4ee82b43eb4847bdc7f43b1e2f8a728cccfc927306`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 7.5 MB (7520601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785c2af96b4fc01fcff0cd0960ddc83afda3cd11b4eec3a21cc4c5f30215e2e`  
		Last Modified: Thu, 04 Jun 2026 18:08:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f4e77f02b0b2fcbcf987a848591e70e1c93f9ef3a55fae5203111033538e9`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 17.9 MB (17931630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3120fd7072b1f1a5d5be20c5a683df43c44a83138de904a218eab97b207504f`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 21.6 MB (21600710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36215de06e3caf20eea3896a736ef62cd8781a6ad29c59b3770861e099c480`  
		Last Modified: Thu, 04 Jun 2026 18:08:56 GMT  
		Size: 10.8 MB (10799590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f2516dcd66747913c10f55b4bbeb888c516fb89a92b053c3cf2b7f7cbf890`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1b58006ea160ba5b1bf10aa23ba231d3cb16e28fa6ad189e87d8346be0a03`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d62d63cdd137a31073061aef2a3c732e4d4f0fec10a30d7d93496a70b0053`  
		Last Modified: Thu, 04 Jun 2026 18:08:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3d7d1e69bcb16737aba3f84171773e55dc5e7293ab857fbbc754e0b61c181`  
		Last Modified: Thu, 04 Jun 2026 18:12:59 GMT  
		Size: 6.6 MB (6577156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35895177edcf0459851a68da3f529aad815c6a06fc487bc78b67925822656c2`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 87.8 KB (87838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76012c6359cf96274f94e94ff4d395f8dcc9562130981ad47924978054b0f083`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a191244d67d45d9772df793ae4c4569cc18daab0aa247288428000db7a4e0a03`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 63.8 MB (63785660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0234b9f18f3e4e53673b485b84b67f0a658a88dc1de10bfe728995844996b`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad57512870cbfde869dda3537d23c6d1056b25b0243b1f2823b31e8771f9a2c`  
		Last Modified: Thu, 04 Jun 2026 18:13:00 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:355b3babed5e09d804da8c33da9f3ed53746277aab8c1e43ecbe44c04cd09668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ccef25134c4f167d669bb33f7132a58a52e45c33d569d7679cdb81f001e0ff`

```dockerfile
```

-	Layers:
	-	`sha256:4eebc04a44848f48946a6c5a194b0c366123dae69712777b204e003616fecb18`  
		Last Modified: Thu, 04 Jun 2026 18:12:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:387297c81bd1610b71e90a377ef6306f213d9262387b4d23883481a1f90a2550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130978501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ab87dbef3dcba50bd1de84ab87396a610d1281dba6f3e67f8ce5452fb2f67`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:07:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jun 2026 18:07:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:07:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jun 2026 18:07:51 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jun 2026 18:07:52 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jun 2026 18:07:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jun 2026 18:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 18:07:53 GMT
CMD ["sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jun 2026 18:12:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9352513a590a2e78c4210d0d52e2405049780151dfb7dc5fb3183688eccffad`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 8.4 MB (8368388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a21f5f0ddd09547849028d73ef09038a0525221bd11bac91cd4f99d1f8549`  
		Last Modified: Thu, 04 Jun 2026 18:07:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24868f55c6a10c79df4721f48274edc18a5117006c974cb10d353e5c7a0d78a2`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 17.8 MB (17764273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed005d3412db7c116546f344d35dab48e16ee052266133cb791b8001ebc52e`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 20.8 MB (20815969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64a3b455b8831db85693edfbd986611eb73f8cc525e43cc52d0c759a2d4773`  
		Last Modified: Thu, 04 Jun 2026 18:08:00 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a429c4ee790c050ca26e4f3dee7a4c90d083bbd8d130fcecd10b2d33736c6`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0d55a86c50ccf66e19cf8a5b54ebb6fae21fe51ff3be5f10746571a8b3498`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2ef9173d00095bdba0db0e4a75db5113a94e3835a006e2da632ab6bf06115`  
		Last Modified: Thu, 04 Jun 2026 18:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85c54ed52d25f4371f9350ee560b4e406973911b494e7537c450ae50893f36`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 7.2 MB (7219850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51d18ca94494dd4d07a8feec72f551d1ad42f849158c136bde50cb897a0cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 100.9 KB (100939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507c3acc77a8b95b8abcc626904f219410b5d27389cc51ca4c2c16a3dfd1e82`  
		Last Modified: Thu, 04 Jun 2026 18:13:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba831d76ec821cdc9987e9685b2decec50ed1989935ff0ac5d86db69697fe4`  
		Last Modified: Thu, 04 Jun 2026 18:13:04 GMT  
		Size: 62.1 MB (62141194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829b6f5c794c36d69bf2f4abc3dd02985bf87df9122c458371c6800aace46cc7`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd24d44a33eb57a4eacc7d6e4084980faf9c70a7e1157db2874c344b09a85f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:03 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:d8a2f66d8cb21198f3c009790c921dd7f1940c10a3ad9d0235741829eb140e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7de24f830a299a1e537977495fbf842b9d31f3e70750c2f2ecd7c274283b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f227e53b9e53c71cc3a11d1d3c57f48e6fbdff69b2751016ea87727251e354e1`  
		Last Modified: Thu, 04 Jun 2026 18:13:01 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:a4506ea88c29d83e0c6f74a20dde3d510d490377feb330023763fc4180ede82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:626792a62ccf43d2c9c9f4106f25ac02fc10678a0f7ba40048484f76cccceb88
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335542989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9b36b1ba1723e3254afdfda83f60d48a67f885c462964ad4e4c9e14caea0a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:08:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:10:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:10:06 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:25 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:46 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:11:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e863137cc1a6c081981346b9911aa1b849767470cdb83cf8038b653b226e5`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13126202d74ea043ab743e8c58bf13f03d98c23877900c616afdb1fcb05ffc`  
		Last Modified: Tue, 09 Jun 2026 22:11:10 GMT  
		Size: 366.6 KB (366612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8450b716d93cc1abde208e2b7bbf780e835eedac6e83b3bf107dd22257e6d4f3`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0798499ee10239ba25cc04fb9b50137e1dc8535b2f0f7d8ec34d61a24e4334`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4335418e7b397c58162055ace3d049acef6d6a75695d40dcf7e1db5adcddc0e4`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 20.0 MB (20005460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82583ec76facc4e8c5d476866755314aac071c25b88ccc0714a9ea28cb9d5916`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c320c84b185908993c2ae455c8e19c447a3440d143e3df1e530688c2f2e48ab`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de253f20eb848fe03012cde3845923b7c3cbd8109b8848bcc65fe1a7e8ec78db`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1070177e1931be03c0bd9b077e590d23aba398d31e78f470b4a25895543ca9`  
		Last Modified: Tue, 09 Jun 2026 22:11:13 GMT  
		Size: 23.9 MB (23917170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44aca9e4206f912e275df50b300bb51b33594cb83228092fd0a1d7fda852d13`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09348bd8a2ac253880aff66aafdd100a7937ef94ecbd671ba62ea967a391c583`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0907212d8ad1bf4caaf2f7d9bae2ab4b6f11ce4bf246f2b3342a04b587941720`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d7087beffaf8878b9474aa75e2c3f844499000ed25a49af03ed7cf6ce3a487`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 12.1 MB (12099197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:e1874ace86696dc406093e614d34ce6a6f07ed7187e25f029685911a711ccc40
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188548521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d76e268d68e640ffd98a8af27bf187fba7876b6ac6253c294854ec499aed056`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:09:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:09:41 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:09:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:09 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:39 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:10:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a21107eb392ad352a11d88add9657687384931e5d889cdcf2e9933b4421077`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b0d166672182721ce571506f9d6ffbdf3978263c1e98a8c7cb83d70e5ceb3`  
		Last Modified: Tue, 09 Jun 2026 22:10:56 GMT  
		Size: 487.8 KB (487761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b460336fce54b4157c40e9e971fab0f408aeda838dde55bcf5ea5de52f3fa3`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea67caacc1b68dc837ec089a76c72de278a12c98986a9e7e27a6b4fa3f1f289`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9755d22906699b3ae49e1e7e643b80a71128ccb86715598896d101848d5074`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 20.0 MB (19967046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa89af8ddf8470a85bb4691fdf78f932741c527c8b8f25d9cdb0ab957b72766`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e31ea216b5955db20bf270de50921353f50fb244567aeffa9aec6a22bdf910`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0473ee7061cd54cff9f36e7d95856e8a0ad754f1afd89c20cff85132b100c5f`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d1bb31a8a58e6c19fa9476763d11417da6c9deccc5f3a25491e741f79611`  
		Last Modified: Tue, 09 Jun 2026 22:11:00 GMT  
		Size: 23.9 MB (23888859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e4bdf749ee7ad62af795111680dbce48097a254a3d53ebee0f0feb07f3820`  
		Last Modified: Tue, 09 Jun 2026 22:10:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdcd68b54960c0145901d3e97fbca29555cdd34359f1433932b88715f7ebd8a`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcecc97fe08a6e5f535dbb042a7e39cee7fd26ff6b8f64f4b87657d71a9ca42`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057fa34c824943d81b41f22bf794e23e40378d1db98addd0261c1fc64a152f55`  
		Last Modified: Tue, 09 Jun 2026 22:10:54 GMT  
		Size: 12.1 MB (12067581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9df2b61e3220bc07763d0d46ea3ea7d312e1e012d5c746cf9686ca44cd8b59cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:e1874ace86696dc406093e614d34ce6a6f07ed7187e25f029685911a711ccc40
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188548521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d76e268d68e640ffd98a8af27bf187fba7876b6ac6253c294854ec499aed056`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:09:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:09:41 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:09:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:09 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:39 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:10:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a21107eb392ad352a11d88add9657687384931e5d889cdcf2e9933b4421077`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b0d166672182721ce571506f9d6ffbdf3978263c1e98a8c7cb83d70e5ceb3`  
		Last Modified: Tue, 09 Jun 2026 22:10:56 GMT  
		Size: 487.8 KB (487761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b460336fce54b4157c40e9e971fab0f408aeda838dde55bcf5ea5de52f3fa3`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea67caacc1b68dc837ec089a76c72de278a12c98986a9e7e27a6b4fa3f1f289`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9755d22906699b3ae49e1e7e643b80a71128ccb86715598896d101848d5074`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 20.0 MB (19967046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa89af8ddf8470a85bb4691fdf78f932741c527c8b8f25d9cdb0ab957b72766`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e31ea216b5955db20bf270de50921353f50fb244567aeffa9aec6a22bdf910`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0473ee7061cd54cff9f36e7d95856e8a0ad754f1afd89c20cff85132b100c5f`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d1bb31a8a58e6c19fa9476763d11417da6c9deccc5f3a25491e741f79611`  
		Last Modified: Tue, 09 Jun 2026 22:11:00 GMT  
		Size: 23.9 MB (23888859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e4bdf749ee7ad62af795111680dbce48097a254a3d53ebee0f0feb07f3820`  
		Last Modified: Tue, 09 Jun 2026 22:10:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdcd68b54960c0145901d3e97fbca29555cdd34359f1433932b88715f7ebd8a`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcecc97fe08a6e5f535dbb042a7e39cee7fd26ff6b8f64f4b87657d71a9ca42`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057fa34c824943d81b41f22bf794e23e40378d1db98addd0261c1fc64a152f55`  
		Last Modified: Tue, 09 Jun 2026 22:10:54 GMT  
		Size: 12.1 MB (12067581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b641303b79f48efd2803ac9c593cdd44c95c59202eb8d7e4380fa6caf293430b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:626792a62ccf43d2c9c9f4106f25ac02fc10678a0f7ba40048484f76cccceb88
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335542989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9b36b1ba1723e3254afdfda83f60d48a67f885c462964ad4e4c9e14caea0a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:08:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:10:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:10:06 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:25 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:26 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:46 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:47 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:11:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e863137cc1a6c081981346b9911aa1b849767470cdb83cf8038b653b226e5`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13126202d74ea043ab743e8c58bf13f03d98c23877900c616afdb1fcb05ffc`  
		Last Modified: Tue, 09 Jun 2026 22:11:10 GMT  
		Size: 366.6 KB (366612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8450b716d93cc1abde208e2b7bbf780e835eedac6e83b3bf107dd22257e6d4f3`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0798499ee10239ba25cc04fb9b50137e1dc8535b2f0f7d8ec34d61a24e4334`  
		Last Modified: Tue, 09 Jun 2026 22:11:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4335418e7b397c58162055ace3d049acef6d6a75695d40dcf7e1db5adcddc0e4`  
		Last Modified: Tue, 09 Jun 2026 22:11:11 GMT  
		Size: 20.0 MB (20005460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82583ec76facc4e8c5d476866755314aac071c25b88ccc0714a9ea28cb9d5916`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c320c84b185908993c2ae455c8e19c447a3440d143e3df1e530688c2f2e48ab`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de253f20eb848fe03012cde3845923b7c3cbd8109b8848bcc65fe1a7e8ec78db`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1070177e1931be03c0bd9b077e590d23aba398d31e78f470b4a25895543ca9`  
		Last Modified: Tue, 09 Jun 2026 22:11:13 GMT  
		Size: 23.9 MB (23917170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44aca9e4206f912e275df50b300bb51b33594cb83228092fd0a1d7fda852d13`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09348bd8a2ac253880aff66aafdd100a7937ef94ecbd671ba62ea967a391c583`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0907212d8ad1bf4caaf2f7d9bae2ab4b6f11ce4bf246f2b3342a04b587941720`  
		Last Modified: Tue, 09 Jun 2026 22:11:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d7087beffaf8878b9474aa75e2c3f844499000ed25a49af03ed7cf6ce3a487`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 12.1 MB (12099197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
