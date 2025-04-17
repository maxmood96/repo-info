<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-1809`](#docker28-windowsservercore-1809)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.1`](#docker281)
-	[`docker:28.1-cli`](#docker281-cli)
-	[`docker:28.1-dind`](#docker281-dind)
-	[`docker:28.1-dind-rootless`](#docker281-dind-rootless)
-	[`docker:28.1-windowsservercore`](#docker281-windowsservercore)
-	[`docker:28.1-windowsservercore-1809`](#docker281-windowsservercore-1809)
-	[`docker:28.1-windowsservercore-ltsc2022`](#docker281-windowsservercore-ltsc2022)
-	[`docker:28.1-windowsservercore-ltsc2025`](#docker281-windowsservercore-ltsc2025)
-	[`docker:28.1.0`](#docker2810)
-	[`docker:28.1.0-alpine3.21`](#docker2810-alpine321)
-	[`docker:28.1.0-cli`](#docker2810-cli)
-	[`docker:28.1.0-cli-alpine3.21`](#docker2810-cli-alpine321)
-	[`docker:28.1.0-dind`](#docker2810-dind)
-	[`docker:28.1.0-dind-alpine3.21`](#docker2810-dind-alpine321)
-	[`docker:28.1.0-dind-rootless`](#docker2810-dind-rootless)
-	[`docker:28.1.0-windowsservercore`](#docker2810-windowsservercore)
-	[`docker:28.1.0-windowsservercore-1809`](#docker2810-windowsservercore-1809)
-	[`docker:28.1.0-windowsservercore-ltsc2022`](#docker2810-windowsservercore-ltsc2022)
-	[`docker:28.1.0-windowsservercore-ltsc2025`](#docker2810-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:4de6a5668da5d138bf9c18b29d2702e43c8773daee085087ba4fac61a6d34b7f
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

### `docker:28` - linux; amd64

```console
$ docker pull docker@sha256:9fb175225e8d3ff95ec41225424d3dcacf78af96544fb2aa2613a78a6d044cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140804349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26e595cb1df199dc05758e494ee8e1aa36bbd2c66b1e203108308187632b9fd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf07815168db14b53eefbc2c3049e107436cd426ee5b782a58f5dc0ce721611`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 8.1 MB (8062915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254bf878645b22853e806a0cb032d9e31d7d1e2fb63fa14996f2997754c4cc1`  
		Last Modified: Tue, 15 Apr 2025 21:57:55 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9c03f587febd06f516e8f5db9bfddcc26cfcb2e46713cd8964afe2cfa28e59`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 19.5 MB (19543064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8295a4327cea935c4c7193578b26fa033a39406088c826cd2d2cfe0f6341`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 21.5 MB (21456665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e931d098a4300b460baecb7bcd9871f0ac28ef04383131312e02105be2a254`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 20.9 MB (20915274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded655ab0883de9cda884f991c3ad2cb6ad71c325da540960fafd7ac2fe3bc5d`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa871cc6f3a41b34ac7bbbf20622b7983dd7eca584ee9afb54b2c8a04e664b9c`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c07c6b0cd3b4ba10c399f3467fd19017a58af5745b971b65c649d678609ce`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f314ec54f4e87b9fdd041baf54da645d0ddf3da9b65fac9f28b0b8c0a461abe`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 6.7 MB (6733013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62802569a7de6fb03151c263562da930e1286fb0532074c74e81abcdfd8c0844`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb73a7dab2ddd6d77007e093ca25de304da091667ee2ceed1d01602287dc96f`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b949978249f4df524390327d0a22df6fbbd2e120040d3496ad9cf7a7e33e68`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 60.4 MB (60352738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104b222ae0f025187b7161d740d6bbc959ea42706a47cf8f9992609b90b0a15`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edee73960c7ecf182956111c4e412314235d1bf7de03c03fb193a66cbb3b805a`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:e9e881fce74013b8bd253845a1123f308d6f43a95f998e5fbcbc2b2a21350efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfc677921894b8bb22e951faa9c6358b561bd410a5a7bf854ea41fdad6ffcf9`

```dockerfile
```

-	Layers:
	-	`sha256:c5b5f23ce5548836116224bb8276806baaa70805aef357537f0c4af866495130`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:53f4029bd5c29e8412956b6a1168de2911e346048db80e9fe36ead17aaa351e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131459597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4dc168e6991627d0696aa634bdd8592b0e0cdc73c003058b3c97501c6085af`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb5ac7b586d2e616a3738487da728728e6ab907dbb55ca806bdbb258bffd4c`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 20.1 MB (20075447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cdba92e4820b290f335e99cc2497c15690be024cf49bfb3e84dae1d3b2f7aa`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 19.7 MB (19668391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f5df8cea3ca65fc59997f2930cee95224e394d2a822ef8fc86c93bc89a42b`  
		Last Modified: Tue, 15 Apr 2025 22:02:04 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd02c5d1daa4616ef9477cdfaf2938c59e4530da64323973c74114d1915a0e8`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784c0d09c497636b078403d01ba86ee45f69ea138e4c38778053cf12831fa589`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6385212aef435bf5fe83c846e5b0f0101cda8a2c35c997d5174641d636035133`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 7.0 MB (7036907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea41391ed39ae4550f757b7a9c4e6e7f72e03a2c84684b9b3af34a3982f0a6b`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 89.9 KB (89855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db336116a24939a7cb10bdd17233d99717160d5a44e329abcb3e1ea5133961a`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c90b7ec9b1e813885cf5d27bf57ec4ab9e7b12f2540f8099f75816b3eee94a`  
		Last Modified: Tue, 15 Apr 2025 22:30:06 GMT  
		Size: 55.7 MB (55741232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9694034f73e287b4e5985ba304e8f73b91060235fbc5598420119799e5464b`  
		Last Modified: Tue, 15 Apr 2025 22:30:05 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf9e7a6fda7047908acb8fca091d9b34be94912a469241a40168f9b789173b`  
		Last Modified: Tue, 15 Apr 2025 22:30:05 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:ba0d9764ae8f75d50f2ea82d950d8295c73ead10541e01d067eb22e4a9894ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52accc0ef60bca4959d92961236c8a7ed81d62a5855d8f91c662a056a8883f06`

```dockerfile
```

-	Layers:
	-	`sha256:19cf11c2a0717b5ca0dd4ab85a6d76e16f7c97b7e2bc73a1d63dd6a4a3c35d91`  
		Last Modified: Tue, 15 Apr 2025 22:30:03 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:2a2e09e827036692beebf4895f76b70ec7107429023bff61dc7e5e4fe13d783c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129795129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282a95b1fcf27a6134f8c92af53d356745663a43fe2972b5db8b40c4dd6934c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a864060af87a5048c5c602ac87964067948691631141ffc3818333edb16ed6`  
		Last Modified: Tue, 15 Apr 2025 22:13:41 GMT  
		Size: 7.3 MB (7301755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c418fb5b9eb8648b75bfdc32d3b64717b14e09489dfedf7e46fc76341ad53`  
		Last Modified: Tue, 15 Apr 2025 22:13:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd85b047c7948100b1f2399a8eea9d8b0b88f7e5be1fb7dc2dafae83f9abc79`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 17.5 MB (17486305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260399ab5d107c45411de9a9bb80ceb98c4127d21afb7d74f09f28159a401c37`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 20.1 MB (20055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac89693fff3745a0f965eeb714910187ffa11d066e9350cd739ac8abd51851`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 19.7 MB (19651336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d180cbaf95968e95d53d1e91cebf8edb96d048a9cf7d70de617dbf1fc294ea7`  
		Last Modified: Tue, 15 Apr 2025 22:14:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0055fbe8376d2bdc3df4d623bcc98e03e488ca7d5b016ad04967401ad02deb`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac853fc592a73bec02462f288dccaffe3e3a3d6df3674ffeac7fc1700698529d`  
		Last Modified: Tue, 15 Apr 2025 22:14:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5184d90f6369c2f5f1e29a37fe3b3fb3e0539b04e800513c8a853d38c650499`  
		Last Modified: Tue, 15 Apr 2025 22:35:10 GMT  
		Size: 6.4 MB (6366053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1acf458da982581dd9b61a4a0956dbee6993e62bba3116184a25fe59a3f733`  
		Last Modified: Tue, 15 Apr 2025 22:35:09 GMT  
		Size: 86.4 KB (86361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c270a2cf682f8879277f147121c3e5d87771a05bc795d9d59f2a6db996a452af`  
		Last Modified: Tue, 15 Apr 2025 22:35:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e7bcdf843369eb576f5159861f0097b833abb7c49fd377711ce5939a7b1de`  
		Last Modified: Tue, 15 Apr 2025 22:35:12 GMT  
		Size: 55.7 MB (55741239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b943e454e66f65972d76e9082ba248befda3168ed13b26a4cbc36e27b35744`  
		Last Modified: Tue, 15 Apr 2025 22:35:11 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753779b323550f5a1e0443228843cf7835bc5d6f2fbd8d1ce67047cebcbae09f`  
		Last Modified: Tue, 15 Apr 2025 22:35:11 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:a0623b4bb16f8485ecdbe795429d3dd4719d250ce0882e82931a6320968e5af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1e2701fe2f97efe7673d949bf676ad4f5eb2da5c330f6e5d4e15815a241d88`

```dockerfile
```

-	Layers:
	-	`sha256:b21d7fb3b31d9e2a5468fc38c926984d475bf91cefe7ab9bd350a7de9119b091`  
		Last Modified: Tue, 15 Apr 2025 22:35:09 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5d4d2e49343b6e3788b1b9dfa0e6510e5787ede7a75621a8eb61dfb409748797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132182786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969af15cd525f0961932384442d28f48239790e80f2ef068806c0cd05b58d192`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e41a332ac34c555abfc416477e260fbde6301802d8e137957166d7b7269e14`  
		Last Modified: Tue, 15 Apr 2025 22:05:00 GMT  
		Size: 8.1 MB (8077251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b44bc2c49279b62c624fcbb004d6fb2af3e11e622deceb7b73b2d962d7213`  
		Last Modified: Tue, 15 Apr 2025 22:04:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548b10c496662caab533c3d131758d622285b3f373756838531f1a168224831`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 18.5 MB (18457152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a45d6fe346d03b0272285dd9725e00aefad8b06d1f295635b39c9630cc6a6`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 19.7 MB (19692478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510dd6065899f34e92a17b88db1cb1ce4b9130bcd36f87ff97a9cfc7cd2430b8`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 19.2 MB (19165660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803567d33d1c34c1f24b0f2ca1c14b4b236cc528d23d4b4e2cd31a71d2d95cf9`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640dbcafae79da65d205c76809ffb4d36184629f730bbfe5390d61bdbb9bb592`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac5cd38945045e3390b31fbbf1b98016e77d70bfc1c8e4943c8a511454f46be`  
		Last Modified: Tue, 15 Apr 2025 22:14:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dc6d9cc98ef412cebe1089c79a0b32ddfed7b3321d6fa49c3b1d7dbe4b3c70`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a9f3b4322221600837bd19350617e9fbdf944b0f97ea579f4969f6e5d6049e`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 99.4 KB (99378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60eb0dce1bf078d608f862da78405ed0a6787825fbd8f9584b22f503dab449c`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ed7a6d0e2d072bf5c0d02797956e1062a2c902e2aab07367bdfe977c466161`  
		Last Modified: Tue, 15 Apr 2025 22:26:03 GMT  
		Size: 55.7 MB (55710879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1e30286ee5a0c6035e171d60a2b4e64cceaf5e8d3b4b7744f47a2c3affcc0`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180e29b0ef2ab0fe57327b9d65d69b7d92b6245d338b4a9eaf59353772f325e`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:704d76da08f415078565b0728f7e1a80695fd64414e71af349d8bbc76e7b85d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3d917794b140e94e3032fe9ad8f6d1045f397961d2a8ef17c4bc86318782f8`

```dockerfile
```

-	Layers:
	-	`sha256:97e71ce1d2497e5c4723f68f9b66746699cc08da3d199b87ca3346f8aa33fa12`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:2bccc79fc5fed23d876bf244fa5fbe78c54bf6b6145a9483604306fd797237d5
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

### `docker:28-cli` - linux; amd64

```console
$ docker pull docker@sha256:983810d28c45d47160a841b12dfb8ba42f96c62495628827dd075d96ac1b1702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73622316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf7b1ff4c923776ce776529a8b25cc898e9866de6cf439c745b63bf74946a05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 15 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf07815168db14b53eefbc2c3049e107436cd426ee5b782a58f5dc0ce721611`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 8.1 MB (8062915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254bf878645b22853e806a0cb032d9e31d7d1e2fb63fa14996f2997754c4cc1`  
		Last Modified: Tue, 15 Apr 2025 21:57:55 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9c03f587febd06f516e8f5db9bfddcc26cfcb2e46713cd8964afe2cfa28e59`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 19.5 MB (19543064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8295a4327cea935c4c7193578b26fa033a39406088c826cd2d2cfe0f6341`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 21.5 MB (21456665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e931d098a4300b460baecb7bcd9871f0ac28ef04383131312e02105be2a254`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 20.9 MB (20915274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded655ab0883de9cda884f991c3ad2cb6ad71c325da540960fafd7ac2fe3bc5d`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa871cc6f3a41b34ac7bbbf20622b7983dd7eca584ee9afb54b2c8a04e664b9c`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c07c6b0cd3b4ba10c399f3467fd19017a58af5745b971b65c649d678609ce`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5afc06789c7da16881d8ff9923362831485e2ef6ffee049455f8ecb0a880f4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e35c86f082c9f994834f1d3228ba17cc676b2b5e49a8f4e9bd258cdbe29b33`

```dockerfile
```

-	Layers:
	-	`sha256:5da8fe9f57c54e87518f03ce91e93eedfec5afcc759f89dc446ca45a3e049368`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a0ed6c56fb060bc8b9b4abedc86e670ad12bd485b23bc4fbcfb0d46b0b3960a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68585632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaf60f8978100f7491ba22ba5b6f5a57900fa12599d6c2e567243feb0f2cb88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 15 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb5ac7b586d2e616a3738487da728728e6ab907dbb55ca806bdbb258bffd4c`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 20.1 MB (20075447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cdba92e4820b290f335e99cc2497c15690be024cf49bfb3e84dae1d3b2f7aa`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 19.7 MB (19668391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f5df8cea3ca65fc59997f2930cee95224e394d2a822ef8fc86c93bc89a42b`  
		Last Modified: Tue, 15 Apr 2025 22:02:04 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd02c5d1daa4616ef9477cdfaf2938c59e4530da64323973c74114d1915a0e8`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784c0d09c497636b078403d01ba86ee45f69ea138e4c38778053cf12831fa589`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c1f90eb72b7c6eaf83d7052d3d93190f5fcf5c9b2437d93f244fd8703ebb2ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92791d992c015a958dddc1c93f19c549684ef1f63730b8a919828add840c257f`

```dockerfile
```

-	Layers:
	-	`sha256:625be85ff5107228c5bbd34a1973b3fcf7d19a0a5b8b1998ef0b81e1250939bb`  
		Last Modified: Tue, 15 Apr 2025 22:02:04 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2af962d764f49e46d9c810b4169ebbde2c4eeab61b12692cb35db46e984c6459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67595521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687d89aaecf25dd10ec0aec7be15ea2150bf9a80dcf011eb8e8fe57a27e9cde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 15 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a864060af87a5048c5c602ac87964067948691631141ffc3818333edb16ed6`  
		Last Modified: Tue, 15 Apr 2025 22:13:41 GMT  
		Size: 7.3 MB (7301755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c418fb5b9eb8648b75bfdc32d3b64717b14e09489dfedf7e46fc76341ad53`  
		Last Modified: Tue, 15 Apr 2025 22:13:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd85b047c7948100b1f2399a8eea9d8b0b88f7e5be1fb7dc2dafae83f9abc79`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 17.5 MB (17486305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260399ab5d107c45411de9a9bb80ceb98c4127d21afb7d74f09f28159a401c37`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 20.1 MB (20055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac89693fff3745a0f965eeb714910187ffa11d066e9350cd739ac8abd51851`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 19.7 MB (19651336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d180cbaf95968e95d53d1e91cebf8edb96d048a9cf7d70de617dbf1fc294ea7`  
		Last Modified: Tue, 15 Apr 2025 22:14:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0055fbe8376d2bdc3df4d623bcc98e03e488ca7d5b016ad04967401ad02deb`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac853fc592a73bec02462f288dccaffe3e3a3d6df3674ffeac7fc1700698529d`  
		Last Modified: Tue, 15 Apr 2025 22:14:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8e04ef7ae685b1199288f01e15370aa9bfc211c0035035b224b1510f62edab6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0b5e2b502ed38e53cdef5900da42c7f075ba2a70cd80f3c4d5be73dce3d524`

```dockerfile
```

-	Layers:
	-	`sha256:77726e7bcd4f853fa91618b8fc71b1bcfe1d1bfb17970413cad5d067d42afeb2`  
		Last Modified: Tue, 15 Apr 2025 22:14:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f8c5a4b6766ec2a942c8f9214c6f98191d0eb6d3c42a91f5f77b548089a1fc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69387727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ecb7d011e3f164d55b47c303dfd72f04e96b5e4d7032bda574104fdc15f67e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 15 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e41a332ac34c555abfc416477e260fbde6301802d8e137957166d7b7269e14`  
		Last Modified: Tue, 15 Apr 2025 22:05:00 GMT  
		Size: 8.1 MB (8077251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b44bc2c49279b62c624fcbb004d6fb2af3e11e622deceb7b73b2d962d7213`  
		Last Modified: Tue, 15 Apr 2025 22:04:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548b10c496662caab533c3d131758d622285b3f373756838531f1a168224831`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 18.5 MB (18457152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a45d6fe346d03b0272285dd9725e00aefad8b06d1f295635b39c9630cc6a6`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 19.7 MB (19692478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510dd6065899f34e92a17b88db1cb1ce4b9130bcd36f87ff97a9cfc7cd2430b8`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 19.2 MB (19165660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803567d33d1c34c1f24b0f2ca1c14b4b236cc528d23d4b4e2cd31a71d2d95cf9`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640dbcafae79da65d205c76809ffb4d36184629f730bbfe5390d61bdbb9bb592`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac5cd38945045e3390b31fbbf1b98016e77d70bfc1c8e4943c8a511454f46be`  
		Last Modified: Tue, 15 Apr 2025 22:14:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:15fb8f2e8e3351a29332a9e5dc5bc0e16656534be3ab802a11caa1460a38529a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86df0fb2d6368f9e61802919f3f8c0eabb1d0701f8e72287b61c2b8f28c25efd`

```dockerfile
```

-	Layers:
	-	`sha256:5d4936c9d50b732e7f62e0cc351a434d0368852afd6a10fb3311ec1be1a766dd`  
		Last Modified: Tue, 15 Apr 2025 22:14:26 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:4de6a5668da5d138bf9c18b29d2702e43c8773daee085087ba4fac61a6d34b7f
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

### `docker:28-dind` - linux; amd64

```console
$ docker pull docker@sha256:9fb175225e8d3ff95ec41225424d3dcacf78af96544fb2aa2613a78a6d044cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140804349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26e595cb1df199dc05758e494ee8e1aa36bbd2c66b1e203108308187632b9fd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf07815168db14b53eefbc2c3049e107436cd426ee5b782a58f5dc0ce721611`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 8.1 MB (8062915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254bf878645b22853e806a0cb032d9e31d7d1e2fb63fa14996f2997754c4cc1`  
		Last Modified: Tue, 15 Apr 2025 21:57:55 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9c03f587febd06f516e8f5db9bfddcc26cfcb2e46713cd8964afe2cfa28e59`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 19.5 MB (19543064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8295a4327cea935c4c7193578b26fa033a39406088c826cd2d2cfe0f6341`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 21.5 MB (21456665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e931d098a4300b460baecb7bcd9871f0ac28ef04383131312e02105be2a254`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 20.9 MB (20915274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded655ab0883de9cda884f991c3ad2cb6ad71c325da540960fafd7ac2fe3bc5d`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa871cc6f3a41b34ac7bbbf20622b7983dd7eca584ee9afb54b2c8a04e664b9c`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c07c6b0cd3b4ba10c399f3467fd19017a58af5745b971b65c649d678609ce`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f314ec54f4e87b9fdd041baf54da645d0ddf3da9b65fac9f28b0b8c0a461abe`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 6.7 MB (6733013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62802569a7de6fb03151c263562da930e1286fb0532074c74e81abcdfd8c0844`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb73a7dab2ddd6d77007e093ca25de304da091667ee2ceed1d01602287dc96f`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b949978249f4df524390327d0a22df6fbbd2e120040d3496ad9cf7a7e33e68`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 60.4 MB (60352738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104b222ae0f025187b7161d740d6bbc959ea42706a47cf8f9992609b90b0a15`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edee73960c7ecf182956111c4e412314235d1bf7de03c03fb193a66cbb3b805a`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e9e881fce74013b8bd253845a1123f308d6f43a95f998e5fbcbc2b2a21350efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfc677921894b8bb22e951faa9c6358b561bd410a5a7bf854ea41fdad6ffcf9`

```dockerfile
```

-	Layers:
	-	`sha256:c5b5f23ce5548836116224bb8276806baaa70805aef357537f0c4af866495130`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:53f4029bd5c29e8412956b6a1168de2911e346048db80e9fe36ead17aaa351e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131459597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4dc168e6991627d0696aa634bdd8592b0e0cdc73c003058b3c97501c6085af`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb5ac7b586d2e616a3738487da728728e6ab907dbb55ca806bdbb258bffd4c`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 20.1 MB (20075447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cdba92e4820b290f335e99cc2497c15690be024cf49bfb3e84dae1d3b2f7aa`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 19.7 MB (19668391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f5df8cea3ca65fc59997f2930cee95224e394d2a822ef8fc86c93bc89a42b`  
		Last Modified: Tue, 15 Apr 2025 22:02:04 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd02c5d1daa4616ef9477cdfaf2938c59e4530da64323973c74114d1915a0e8`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784c0d09c497636b078403d01ba86ee45f69ea138e4c38778053cf12831fa589`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6385212aef435bf5fe83c846e5b0f0101cda8a2c35c997d5174641d636035133`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 7.0 MB (7036907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea41391ed39ae4550f757b7a9c4e6e7f72e03a2c84684b9b3af34a3982f0a6b`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 89.9 KB (89855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db336116a24939a7cb10bdd17233d99717160d5a44e329abcb3e1ea5133961a`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c90b7ec9b1e813885cf5d27bf57ec4ab9e7b12f2540f8099f75816b3eee94a`  
		Last Modified: Tue, 15 Apr 2025 22:30:06 GMT  
		Size: 55.7 MB (55741232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9694034f73e287b4e5985ba304e8f73b91060235fbc5598420119799e5464b`  
		Last Modified: Tue, 15 Apr 2025 22:30:05 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf9e7a6fda7047908acb8fca091d9b34be94912a469241a40168f9b789173b`  
		Last Modified: Tue, 15 Apr 2025 22:30:05 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ba0d9764ae8f75d50f2ea82d950d8295c73ead10541e01d067eb22e4a9894ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52accc0ef60bca4959d92961236c8a7ed81d62a5855d8f91c662a056a8883f06`

```dockerfile
```

-	Layers:
	-	`sha256:19cf11c2a0717b5ca0dd4ab85a6d76e16f7c97b7e2bc73a1d63dd6a4a3c35d91`  
		Last Modified: Tue, 15 Apr 2025 22:30:03 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:2a2e09e827036692beebf4895f76b70ec7107429023bff61dc7e5e4fe13d783c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129795129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282a95b1fcf27a6134f8c92af53d356745663a43fe2972b5db8b40c4dd6934c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a864060af87a5048c5c602ac87964067948691631141ffc3818333edb16ed6`  
		Last Modified: Tue, 15 Apr 2025 22:13:41 GMT  
		Size: 7.3 MB (7301755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c418fb5b9eb8648b75bfdc32d3b64717b14e09489dfedf7e46fc76341ad53`  
		Last Modified: Tue, 15 Apr 2025 22:13:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd85b047c7948100b1f2399a8eea9d8b0b88f7e5be1fb7dc2dafae83f9abc79`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 17.5 MB (17486305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260399ab5d107c45411de9a9bb80ceb98c4127d21afb7d74f09f28159a401c37`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 20.1 MB (20055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac89693fff3745a0f965eeb714910187ffa11d066e9350cd739ac8abd51851`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 19.7 MB (19651336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d180cbaf95968e95d53d1e91cebf8edb96d048a9cf7d70de617dbf1fc294ea7`  
		Last Modified: Tue, 15 Apr 2025 22:14:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0055fbe8376d2bdc3df4d623bcc98e03e488ca7d5b016ad04967401ad02deb`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac853fc592a73bec02462f288dccaffe3e3a3d6df3674ffeac7fc1700698529d`  
		Last Modified: Tue, 15 Apr 2025 22:14:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5184d90f6369c2f5f1e29a37fe3b3fb3e0539b04e800513c8a853d38c650499`  
		Last Modified: Tue, 15 Apr 2025 22:35:10 GMT  
		Size: 6.4 MB (6366053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1acf458da982581dd9b61a4a0956dbee6993e62bba3116184a25fe59a3f733`  
		Last Modified: Tue, 15 Apr 2025 22:35:09 GMT  
		Size: 86.4 KB (86361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c270a2cf682f8879277f147121c3e5d87771a05bc795d9d59f2a6db996a452af`  
		Last Modified: Tue, 15 Apr 2025 22:35:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e7bcdf843369eb576f5159861f0097b833abb7c49fd377711ce5939a7b1de`  
		Last Modified: Tue, 15 Apr 2025 22:35:12 GMT  
		Size: 55.7 MB (55741239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b943e454e66f65972d76e9082ba248befda3168ed13b26a4cbc36e27b35744`  
		Last Modified: Tue, 15 Apr 2025 22:35:11 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753779b323550f5a1e0443228843cf7835bc5d6f2fbd8d1ce67047cebcbae09f`  
		Last Modified: Tue, 15 Apr 2025 22:35:11 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a0623b4bb16f8485ecdbe795429d3dd4719d250ce0882e82931a6320968e5af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1e2701fe2f97efe7673d949bf676ad4f5eb2da5c330f6e5d4e15815a241d88`

```dockerfile
```

-	Layers:
	-	`sha256:b21d7fb3b31d9e2a5468fc38c926984d475bf91cefe7ab9bd350a7de9119b091`  
		Last Modified: Tue, 15 Apr 2025 22:35:09 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5d4d2e49343b6e3788b1b9dfa0e6510e5787ede7a75621a8eb61dfb409748797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132182786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969af15cd525f0961932384442d28f48239790e80f2ef068806c0cd05b58d192`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e41a332ac34c555abfc416477e260fbde6301802d8e137957166d7b7269e14`  
		Last Modified: Tue, 15 Apr 2025 22:05:00 GMT  
		Size: 8.1 MB (8077251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b44bc2c49279b62c624fcbb004d6fb2af3e11e622deceb7b73b2d962d7213`  
		Last Modified: Tue, 15 Apr 2025 22:04:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548b10c496662caab533c3d131758d622285b3f373756838531f1a168224831`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 18.5 MB (18457152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a45d6fe346d03b0272285dd9725e00aefad8b06d1f295635b39c9630cc6a6`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 19.7 MB (19692478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510dd6065899f34e92a17b88db1cb1ce4b9130bcd36f87ff97a9cfc7cd2430b8`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 19.2 MB (19165660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803567d33d1c34c1f24b0f2ca1c14b4b236cc528d23d4b4e2cd31a71d2d95cf9`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640dbcafae79da65d205c76809ffb4d36184629f730bbfe5390d61bdbb9bb592`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac5cd38945045e3390b31fbbf1b98016e77d70bfc1c8e4943c8a511454f46be`  
		Last Modified: Tue, 15 Apr 2025 22:14:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dc6d9cc98ef412cebe1089c79a0b32ddfed7b3321d6fa49c3b1d7dbe4b3c70`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a9f3b4322221600837bd19350617e9fbdf944b0f97ea579f4969f6e5d6049e`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 99.4 KB (99378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60eb0dce1bf078d608f862da78405ed0a6787825fbd8f9584b22f503dab449c`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ed7a6d0e2d072bf5c0d02797956e1062a2c902e2aab07367bdfe977c466161`  
		Last Modified: Tue, 15 Apr 2025 22:26:03 GMT  
		Size: 55.7 MB (55710879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1e30286ee5a0c6035e171d60a2b4e64cceaf5e8d3b4b7744f47a2c3affcc0`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180e29b0ef2ab0fe57327b9d65d69b7d92b6245d338b4a9eaf59353772f325e`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:704d76da08f415078565b0728f7e1a80695fd64414e71af349d8bbc76e7b85d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3d917794b140e94e3032fe9ad8f6d1045f397961d2a8ef17c4bc86318782f8`

```dockerfile
```

-	Layers:
	-	`sha256:97e71ce1d2497e5c4723f68f9b66746699cc08da3d199b87ca3346f8aa33fa12`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:b657df8f8aad102f8bc05908deb58402ec791eeffe7b4470e5d576f0e6743765
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:54db6d9791dffefd0b528527b4ed346ae1135a7a05aa8e6da053c1f07314087e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158963462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67318ae1c4af8b4ee0f8bfee72355afe97fb8edaca0fc9265a4ff060b4e0ca3a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf07815168db14b53eefbc2c3049e107436cd426ee5b782a58f5dc0ce721611`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 8.1 MB (8062915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254bf878645b22853e806a0cb032d9e31d7d1e2fb63fa14996f2997754c4cc1`  
		Last Modified: Tue, 15 Apr 2025 21:57:55 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9c03f587febd06f516e8f5db9bfddcc26cfcb2e46713cd8964afe2cfa28e59`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 19.5 MB (19543064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8295a4327cea935c4c7193578b26fa033a39406088c826cd2d2cfe0f6341`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 21.5 MB (21456665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e931d098a4300b460baecb7bcd9871f0ac28ef04383131312e02105be2a254`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 20.9 MB (20915274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded655ab0883de9cda884f991c3ad2cb6ad71c325da540960fafd7ac2fe3bc5d`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa871cc6f3a41b34ac7bbbf20622b7983dd7eca584ee9afb54b2c8a04e664b9c`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c07c6b0cd3b4ba10c399f3467fd19017a58af5745b971b65c649d678609ce`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f314ec54f4e87b9fdd041baf54da645d0ddf3da9b65fac9f28b0b8c0a461abe`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 6.7 MB (6733013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62802569a7de6fb03151c263562da930e1286fb0532074c74e81abcdfd8c0844`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb73a7dab2ddd6d77007e093ca25de304da091667ee2ceed1d01602287dc96f`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b949978249f4df524390327d0a22df6fbbd2e120040d3496ad9cf7a7e33e68`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 60.4 MB (60352738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104b222ae0f025187b7161d740d6bbc959ea42706a47cf8f9992609b90b0a15`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edee73960c7ecf182956111c4e412314235d1bf7de03c03fb193a66cbb3b805a`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbcaf9af1c4542b39548057db3f89ae883e4e42939e64d7809846eed60d4901`  
		Last Modified: Tue, 15 Apr 2025 22:07:45 GMT  
		Size: 986.6 KB (986581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5afaf14a7ec7e06da772bfe38b6f176ff48c453aa74c27de975da807227f52`  
		Last Modified: Tue, 15 Apr 2025 22:07:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdb8f0bdf277c33789ad7e6bb8fce62ba7dd2c92b55e56b0dd61bbd48cc6c1f`  
		Last Modified: Tue, 15 Apr 2025 22:07:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318db3731ff5e1712ab1830de247b8de7a02438f87fcacc4f38fa130f07e2d2a`  
		Last Modified: Tue, 15 Apr 2025 22:07:46 GMT  
		Size: 17.2 MB (17171190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78277d8b957a21553e462b53bbdafb59e66dd775c13421cf61a32a2018941610`  
		Last Modified: Tue, 15 Apr 2025 22:07:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:18aebec3500d96ffee670ca9cf9d842f9123222ce6f5231e4495502266c16c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff35a275e95e551cee5b91de19401fccefa589d3449daee2aafcbfd59fe8df5c`

```dockerfile
```

-	Layers:
	-	`sha256:4a83080acbcd380cf2c01a825d8a390ff7cf4b9c2f4ea899b691d728c0edeaa1`  
		Last Modified: Tue, 15 Apr 2025 22:07:45 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1ff1b98f479dc58cfed04fb991acff688f27a33361568286d93f4b2bf7c43acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152480473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83441b3def8697388a05af1983ee55c6a63d6b2d35756fd153f06c58041d6aec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e41a332ac34c555abfc416477e260fbde6301802d8e137957166d7b7269e14`  
		Last Modified: Tue, 15 Apr 2025 22:05:00 GMT  
		Size: 8.1 MB (8077251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b44bc2c49279b62c624fcbb004d6fb2af3e11e622deceb7b73b2d962d7213`  
		Last Modified: Tue, 15 Apr 2025 22:04:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548b10c496662caab533c3d131758d622285b3f373756838531f1a168224831`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 18.5 MB (18457152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a45d6fe346d03b0272285dd9725e00aefad8b06d1f295635b39c9630cc6a6`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 19.7 MB (19692478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510dd6065899f34e92a17b88db1cb1ce4b9130bcd36f87ff97a9cfc7cd2430b8`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 19.2 MB (19165660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803567d33d1c34c1f24b0f2ca1c14b4b236cc528d23d4b4e2cd31a71d2d95cf9`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640dbcafae79da65d205c76809ffb4d36184629f730bbfe5390d61bdbb9bb592`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac5cd38945045e3390b31fbbf1b98016e77d70bfc1c8e4943c8a511454f46be`  
		Last Modified: Tue, 15 Apr 2025 22:14:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dc6d9cc98ef412cebe1089c79a0b32ddfed7b3321d6fa49c3b1d7dbe4b3c70`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a9f3b4322221600837bd19350617e9fbdf944b0f97ea579f4969f6e5d6049e`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 99.4 KB (99378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60eb0dce1bf078d608f862da78405ed0a6787825fbd8f9584b22f503dab449c`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ed7a6d0e2d072bf5c0d02797956e1062a2c902e2aab07367bdfe977c466161`  
		Last Modified: Tue, 15 Apr 2025 22:26:03 GMT  
		Size: 55.7 MB (55710879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1e30286ee5a0c6035e171d60a2b4e64cceaf5e8d3b4b7744f47a2c3affcc0`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180e29b0ef2ab0fe57327b9d65d69b7d92b6245d338b4a9eaf59353772f325e`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593538725234e7f5471d5edcd1545b428c2be3e765746760f8fbaea46b2965a9`  
		Last Modified: Tue, 15 Apr 2025 23:07:21 GMT  
		Size: 1.0 MB (1014211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f87db4b1a10e689b727a320ef2869a263d4e8c3dc046cd0976435e2d34d983`  
		Last Modified: Tue, 15 Apr 2025 23:07:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48c5275d28148d3c58af76a48d45befc03d686c8647f4569a07da472d3fb932`  
		Last Modified: Tue, 15 Apr 2025 23:07:21 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f1b4eeca171dd968721ebed2f30758cc913ca1fc968d32aaec90b0e4501fc0`  
		Last Modified: Tue, 15 Apr 2025 23:07:22 GMT  
		Size: 19.3 MB (19282132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19c98b4578bd75541d368745c684355023aeed914370664c16ce434016cefa6`  
		Last Modified: Tue, 15 Apr 2025 23:07:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:de3d621c088272cc86d5c7777395aceab3af8e685ee6605b4f4011e6b8f02f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724e2934dbdc120f6444a7c1e06fb77a2ebb3194079761af1ea85196deb8f8c6`

```dockerfile
```

-	Layers:
	-	`sha256:6afe9376f42157faae689cdd015195db7c251375305753dc292b96e889342beb`  
		Last Modified: Tue, 15 Apr 2025 23:07:20 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:528a394441b948ca8fa2ccce01b95f52233729ab27342fb1aa0339e63eac858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8aa47cd924b443e6ed4f2293a2350df34e37e3840d7f2d10fa31ee848767b822
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459291937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554c35c4d3f914e6695b9b090d2e9d3f4038ed0707cc2979c1a8536f166c3b58`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Tue, 15 Apr 2025 22:05:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:05:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:05:42 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:05:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:06:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:06:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:06:31 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:06:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:07:24 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:08:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff803ad22e0ab64f102a722831537db638cc47772e62fa4f66ffc6a1de17bea`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650f48f4339554104a9b685c62ece86c0131ae6c202350e5f1a52e3a37ce006`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 405.2 KB (405161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc49ea6a08f7cb24b63b58139a6dd7d541e4be2c493b13edb6baeadc60ec9d`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d558fa4719a5fac8b7e21cdb0c03d7fb86edd8d43dc1def3abb70c02fcb75805`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148fc3d5ca192103ee3ae1835ce8a09f63c602ef431fcd5e749aa31c35237cdc`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 19.9 MB (19909526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71983d7eafa2374ca5c49782e81dfe35e5039870e7cd99abd2974726f1abdda7`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f2a4a7cef42383900d86e61ce89a2cc511ce078fbd6ef543452b57decc48f6`  
		Last Modified: Tue, 15 Apr 2025 22:08:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb3b7cf9449e0a48b9b27cc9b0f6deece3b5fbe51dd4f277c9570e360b2184f`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb088745c9e5fe660fc7a745b3a9a54607c55d7bae09a18c30a152001e325528`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 22.4 MB (22401686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90041ef92672e9384ec94e0d96df6bb0002534b8aeefcfb5a4d714743ef3706f`  
		Last Modified: Tue, 15 Apr 2025 22:08:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70fc9c300e4e7129f577f4f0812ba764164930ed15018563351f6be609e05d5`  
		Last Modified: Tue, 15 Apr 2025 22:08:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efa5c78927c877cdbd1b451ae71d849f427bfdc3c04a356a4c4bb65152dc2d4`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c4122ecb346154069beaab3457ca61e4629a9de2c32cbeb64f92387e9c96a2`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 21.9 MB (21884365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:68e38ab953a87c61b66914217106b383daee357c4c05b1647ab3a95bfe7d79ce
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335455807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbf36de339df80f34209544c9b63f8b7d83ca23f9337314dfe2eaf417fd644b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Tue, 15 Apr 2025 22:07:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:07:48 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:07:49 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:07:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:07:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:08:00 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:08:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:08:01 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:08:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:08:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:08:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:08:10 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:08:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30151e3643fba377542afac5a171a0527fd990206b8e89128562f09c6b6f761f`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4725ce2acf24e3219acaaa964606e83f8b4a7f2ff49c13f3261a641951a8b1db`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 365.7 KB (365726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9b91c0fe3a715c4879fa6fff556bfc191f884bdcdf19bbdbac4be05eab6fd`  
		Last Modified: Tue, 15 Apr 2025 22:08:25 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919b934268d7cf70b58919f0e50f2a45315bff20b5f9b7e83faca5460b955586`  
		Last Modified: Tue, 15 Apr 2025 22:08:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6737480d00e37347bf879f9271d4ebf5445bd23e5631768e209d02fabc332cf5`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 19.9 MB (19871309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbdcff4db952a6d899885eb2d490f38cc558e145ddd9895b34fdd6d7f8e7c87`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c7b3a352e7efdbbbb5c2e6eeea9ed5deb2f375780a083421b2a6d863238125`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45f0f2eb53c4197068fb31b358a34a63517e22eef46f899066d3417c1f86c05`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07362729c8326851ce50b1c80ca2976934c0ccdee6a27216870ecc812ea693de`  
		Last Modified: Tue, 15 Apr 2025 22:08:24 GMT  
		Size: 22.4 MB (22364101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c09098cac7c45c8f6f1cf5d8e638a25be610c8efd36fe246f0cf0097b1bfde1`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ceaf713f2cf3069d80077b0c0dce7dd6b385d96f318a7fd5b600daf6953008d`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef372443d99cb8ae017ed4b09096ce301d468ff7d48f33711ffa40177c21a85`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc61b0ba2c5210eb8100bc7189348241ae40e963445358cf48edf32774055787`  
		Last Modified: Tue, 15 Apr 2025 22:08:24 GMT  
		Size: 21.8 MB (21847429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:9eea48e8624f5a89b632b349df9a9ef60250b1c5ffa205d3d91cf43c32846ccd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227127342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785c3dec269da97ebda3793c1818235279080fd52a121be171f0b57b16ddba27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Tue, 15 Apr 2025 22:12:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:13:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:13:23 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:13:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:13:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:39 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:13:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:13:41 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:13:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:14:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75559a6ab4985605769e9345e4dff1b1dcce036c5e3f010989bc5d815bcf22db`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbc5225e1556802cd30f8fd34e34314e3d8b61a8646572689a40d59b303a269`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 341.5 KB (341494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5c9f84290e2fafec5927a5d6d17a3a064c93078c593270106ea74ad23ec29a`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bcf429ac4797944cc945ce64dc94e477c8d14341b6fecaf29b9ccc44180cb2`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a44bd61aef7b941f7614c31fb50b8660886b2740bbb23a09d281aef1f08832b`  
		Last Modified: Tue, 15 Apr 2025 22:14:11 GMT  
		Size: 19.9 MB (19860556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d18acc9d9a4944f4b68e2eb3b2056dc918d4f3155a9de9469b804883c9a870`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9fb93169fb4009bfe58fef0cb707780bf6d1452c6b71e4add92e8c230fd923`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d2981dd79b2395c71b1f2abf10aa7e31aafcd81b94c306767eb6394e5caf23`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a04a74dc2f144ff9e196e62a1c06e6277d5004443ce5b7de37e0d4aaa59a13b`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 22.4 MB (22354530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d80f4121c811468ee950acee266056e1e05a0e7ed4750dba28b1290f9444c9`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86e7151feda14da9b65f7fa4811a3d9f596a3f632eee42ca1a9173930178878`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62c931e923807455c87709bcd05a0d7067b18b8f1033c6fc5bb4f1d77c0d98b`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a55036ef8e12942d5bc9f5782020380597b798bdec106fbd29daa958030524`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 21.8 MB (21833195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:6fed54b785c39f7c584b70ac3c8ff8859e0f3517dcc298ea0f3bebcf7e205572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:9eea48e8624f5a89b632b349df9a9ef60250b1c5ffa205d3d91cf43c32846ccd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227127342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785c3dec269da97ebda3793c1818235279080fd52a121be171f0b57b16ddba27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Tue, 15 Apr 2025 22:12:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:13:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:13:23 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:13:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:13:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:39 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:13:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:13:41 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:13:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:14:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75559a6ab4985605769e9345e4dff1b1dcce036c5e3f010989bc5d815bcf22db`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbc5225e1556802cd30f8fd34e34314e3d8b61a8646572689a40d59b303a269`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 341.5 KB (341494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5c9f84290e2fafec5927a5d6d17a3a064c93078c593270106ea74ad23ec29a`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bcf429ac4797944cc945ce64dc94e477c8d14341b6fecaf29b9ccc44180cb2`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a44bd61aef7b941f7614c31fb50b8660886b2740bbb23a09d281aef1f08832b`  
		Last Modified: Tue, 15 Apr 2025 22:14:11 GMT  
		Size: 19.9 MB (19860556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d18acc9d9a4944f4b68e2eb3b2056dc918d4f3155a9de9469b804883c9a870`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9fb93169fb4009bfe58fef0cb707780bf6d1452c6b71e4add92e8c230fd923`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d2981dd79b2395c71b1f2abf10aa7e31aafcd81b94c306767eb6394e5caf23`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a04a74dc2f144ff9e196e62a1c06e6277d5004443ce5b7de37e0d4aaa59a13b`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 22.4 MB (22354530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d80f4121c811468ee950acee266056e1e05a0e7ed4750dba28b1290f9444c9`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86e7151feda14da9b65f7fa4811a3d9f596a3f632eee42ca1a9173930178878`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62c931e923807455c87709bcd05a0d7067b18b8f1033c6fc5bb4f1d77c0d98b`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a55036ef8e12942d5bc9f5782020380597b798bdec106fbd29daa958030524`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 21.8 MB (21833195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:01607c0fe392d1b599a20ff0eaa2cb95b736b9178f561477ca918103bb8d1d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:68e38ab953a87c61b66914217106b383daee357c4c05b1647ab3a95bfe7d79ce
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335455807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbf36de339df80f34209544c9b63f8b7d83ca23f9337314dfe2eaf417fd644b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Tue, 15 Apr 2025 22:07:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:07:48 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:07:49 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:07:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:07:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:08:00 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:08:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:08:01 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:08:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:08:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:08:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:08:10 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:08:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30151e3643fba377542afac5a171a0527fd990206b8e89128562f09c6b6f761f`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4725ce2acf24e3219acaaa964606e83f8b4a7f2ff49c13f3261a641951a8b1db`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 365.7 KB (365726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9b91c0fe3a715c4879fa6fff556bfc191f884bdcdf19bbdbac4be05eab6fd`  
		Last Modified: Tue, 15 Apr 2025 22:08:25 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919b934268d7cf70b58919f0e50f2a45315bff20b5f9b7e83faca5460b955586`  
		Last Modified: Tue, 15 Apr 2025 22:08:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6737480d00e37347bf879f9271d4ebf5445bd23e5631768e209d02fabc332cf5`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 19.9 MB (19871309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbdcff4db952a6d899885eb2d490f38cc558e145ddd9895b34fdd6d7f8e7c87`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c7b3a352e7efdbbbb5c2e6eeea9ed5deb2f375780a083421b2a6d863238125`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45f0f2eb53c4197068fb31b358a34a63517e22eef46f899066d3417c1f86c05`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07362729c8326851ce50b1c80ca2976934c0ccdee6a27216870ecc812ea693de`  
		Last Modified: Tue, 15 Apr 2025 22:08:24 GMT  
		Size: 22.4 MB (22364101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c09098cac7c45c8f6f1cf5d8e638a25be610c8efd36fe246f0cf0097b1bfde1`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ceaf713f2cf3069d80077b0c0dce7dd6b385d96f318a7fd5b600daf6953008d`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef372443d99cb8ae017ed4b09096ce301d468ff7d48f33711ffa40177c21a85`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc61b0ba2c5210eb8100bc7189348241ae40e963445358cf48edf32774055787`  
		Last Modified: Tue, 15 Apr 2025 22:08:24 GMT  
		Size: 21.8 MB (21847429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:eaa298de788f906bf4dcaba103c3a6b9102985e0ba21d3c89c6523fd4b944435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8aa47cd924b443e6ed4f2293a2350df34e37e3840d7f2d10fa31ee848767b822
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459291937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554c35c4d3f914e6695b9b090d2e9d3f4038ed0707cc2979c1a8536f166c3b58`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Tue, 15 Apr 2025 22:05:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:05:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:05:42 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:05:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:06:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:06:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:06:31 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:06:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:07:24 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:08:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff803ad22e0ab64f102a722831537db638cc47772e62fa4f66ffc6a1de17bea`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650f48f4339554104a9b685c62ece86c0131ae6c202350e5f1a52e3a37ce006`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 405.2 KB (405161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc49ea6a08f7cb24b63b58139a6dd7d541e4be2c493b13edb6baeadc60ec9d`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d558fa4719a5fac8b7e21cdb0c03d7fb86edd8d43dc1def3abb70c02fcb75805`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148fc3d5ca192103ee3ae1835ce8a09f63c602ef431fcd5e749aa31c35237cdc`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 19.9 MB (19909526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71983d7eafa2374ca5c49782e81dfe35e5039870e7cd99abd2974726f1abdda7`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f2a4a7cef42383900d86e61ce89a2cc511ce078fbd6ef543452b57decc48f6`  
		Last Modified: Tue, 15 Apr 2025 22:08:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb3b7cf9449e0a48b9b27cc9b0f6deece3b5fbe51dd4f277c9570e360b2184f`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb088745c9e5fe660fc7a745b3a9a54607c55d7bae09a18c30a152001e325528`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 22.4 MB (22401686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90041ef92672e9384ec94e0d96df6bb0002534b8aeefcfb5a4d714743ef3706f`  
		Last Modified: Tue, 15 Apr 2025 22:08:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70fc9c300e4e7129f577f4f0812ba764164930ed15018563351f6be609e05d5`  
		Last Modified: Tue, 15 Apr 2025 22:08:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efa5c78927c877cdbd1b451ae71d849f427bfdc3c04a356a4c4bb65152dc2d4`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c4122ecb346154069beaab3457ca61e4629a9de2c32cbeb64f92387e9c96a2`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 21.9 MB (21884365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.1`

**does not exist** (yet?)

## `docker:28.1-cli`

**does not exist** (yet?)

## `docker:28.1-dind`

**does not exist** (yet?)

## `docker:28.1-dind-rootless`

**does not exist** (yet?)

## `docker:28.1-windowsservercore`

**does not exist** (yet?)

## `docker:28.1-windowsservercore-1809`

**does not exist** (yet?)

## `docker:28.1-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:28.1-windowsservercore-ltsc2025`

**does not exist** (yet?)

## `docker:28.1.0`

**does not exist** (yet?)

## `docker:28.1.0-alpine3.21`

**does not exist** (yet?)

## `docker:28.1.0-cli`

**does not exist** (yet?)

## `docker:28.1.0-cli-alpine3.21`

**does not exist** (yet?)

## `docker:28.1.0-dind`

**does not exist** (yet?)

## `docker:28.1.0-dind-alpine3.21`

**does not exist** (yet?)

## `docker:28.1.0-dind-rootless`

**does not exist** (yet?)

## `docker:28.1.0-windowsservercore`

**does not exist** (yet?)

## `docker:28.1.0-windowsservercore-1809`

**does not exist** (yet?)

## `docker:28.1.0-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:28.1.0-windowsservercore-ltsc2025`

**does not exist** (yet?)

## `docker:cli`

```console
$ docker pull docker@sha256:2bccc79fc5fed23d876bf244fa5fbe78c54bf6b6145a9483604306fd797237d5
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
$ docker pull docker@sha256:983810d28c45d47160a841b12dfb8ba42f96c62495628827dd075d96ac1b1702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73622316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf7b1ff4c923776ce776529a8b25cc898e9866de6cf439c745b63bf74946a05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 15 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf07815168db14b53eefbc2c3049e107436cd426ee5b782a58f5dc0ce721611`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 8.1 MB (8062915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254bf878645b22853e806a0cb032d9e31d7d1e2fb63fa14996f2997754c4cc1`  
		Last Modified: Tue, 15 Apr 2025 21:57:55 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9c03f587febd06f516e8f5db9bfddcc26cfcb2e46713cd8964afe2cfa28e59`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 19.5 MB (19543064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8295a4327cea935c4c7193578b26fa033a39406088c826cd2d2cfe0f6341`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 21.5 MB (21456665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e931d098a4300b460baecb7bcd9871f0ac28ef04383131312e02105be2a254`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 20.9 MB (20915274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded655ab0883de9cda884f991c3ad2cb6ad71c325da540960fafd7ac2fe3bc5d`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa871cc6f3a41b34ac7bbbf20622b7983dd7eca584ee9afb54b2c8a04e664b9c`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c07c6b0cd3b4ba10c399f3467fd19017a58af5745b971b65c649d678609ce`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:5afc06789c7da16881d8ff9923362831485e2ef6ffee049455f8ecb0a880f4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e35c86f082c9f994834f1d3228ba17cc676b2b5e49a8f4e9bd258cdbe29b33`

```dockerfile
```

-	Layers:
	-	`sha256:5da8fe9f57c54e87518f03ce91e93eedfec5afcc759f89dc446ca45a3e049368`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a0ed6c56fb060bc8b9b4abedc86e670ad12bd485b23bc4fbcfb0d46b0b3960a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68585632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaf60f8978100f7491ba22ba5b6f5a57900fa12599d6c2e567243feb0f2cb88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 15 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb5ac7b586d2e616a3738487da728728e6ab907dbb55ca806bdbb258bffd4c`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 20.1 MB (20075447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cdba92e4820b290f335e99cc2497c15690be024cf49bfb3e84dae1d3b2f7aa`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 19.7 MB (19668391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f5df8cea3ca65fc59997f2930cee95224e394d2a822ef8fc86c93bc89a42b`  
		Last Modified: Tue, 15 Apr 2025 22:02:04 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd02c5d1daa4616ef9477cdfaf2938c59e4530da64323973c74114d1915a0e8`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784c0d09c497636b078403d01ba86ee45f69ea138e4c38778053cf12831fa589`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:c1f90eb72b7c6eaf83d7052d3d93190f5fcf5c9b2437d93f244fd8703ebb2ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92791d992c015a958dddc1c93f19c549684ef1f63730b8a919828add840c257f`

```dockerfile
```

-	Layers:
	-	`sha256:625be85ff5107228c5bbd34a1973b3fcf7d19a0a5b8b1998ef0b81e1250939bb`  
		Last Modified: Tue, 15 Apr 2025 22:02:04 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2af962d764f49e46d9c810b4169ebbde2c4eeab61b12692cb35db46e984c6459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67595521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687d89aaecf25dd10ec0aec7be15ea2150bf9a80dcf011eb8e8fe57a27e9cde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 15 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a864060af87a5048c5c602ac87964067948691631141ffc3818333edb16ed6`  
		Last Modified: Tue, 15 Apr 2025 22:13:41 GMT  
		Size: 7.3 MB (7301755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c418fb5b9eb8648b75bfdc32d3b64717b14e09489dfedf7e46fc76341ad53`  
		Last Modified: Tue, 15 Apr 2025 22:13:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd85b047c7948100b1f2399a8eea9d8b0b88f7e5be1fb7dc2dafae83f9abc79`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 17.5 MB (17486305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260399ab5d107c45411de9a9bb80ceb98c4127d21afb7d74f09f28159a401c37`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 20.1 MB (20055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac89693fff3745a0f965eeb714910187ffa11d066e9350cd739ac8abd51851`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 19.7 MB (19651336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d180cbaf95968e95d53d1e91cebf8edb96d048a9cf7d70de617dbf1fc294ea7`  
		Last Modified: Tue, 15 Apr 2025 22:14:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0055fbe8376d2bdc3df4d623bcc98e03e488ca7d5b016ad04967401ad02deb`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac853fc592a73bec02462f288dccaffe3e3a3d6df3674ffeac7fc1700698529d`  
		Last Modified: Tue, 15 Apr 2025 22:14:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:8e04ef7ae685b1199288f01e15370aa9bfc211c0035035b224b1510f62edab6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0b5e2b502ed38e53cdef5900da42c7f075ba2a70cd80f3c4d5be73dce3d524`

```dockerfile
```

-	Layers:
	-	`sha256:77726e7bcd4f853fa91618b8fc71b1bcfe1d1bfb17970413cad5d067d42afeb2`  
		Last Modified: Tue, 15 Apr 2025 22:14:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f8c5a4b6766ec2a942c8f9214c6f98191d0eb6d3c42a91f5f77b548089a1fc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69387727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ecb7d011e3f164d55b47c303dfd72f04e96b5e4d7032bda574104fdc15f67e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 15 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 15 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e41a332ac34c555abfc416477e260fbde6301802d8e137957166d7b7269e14`  
		Last Modified: Tue, 15 Apr 2025 22:05:00 GMT  
		Size: 8.1 MB (8077251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b44bc2c49279b62c624fcbb004d6fb2af3e11e622deceb7b73b2d962d7213`  
		Last Modified: Tue, 15 Apr 2025 22:04:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548b10c496662caab533c3d131758d622285b3f373756838531f1a168224831`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 18.5 MB (18457152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a45d6fe346d03b0272285dd9725e00aefad8b06d1f295635b39c9630cc6a6`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 19.7 MB (19692478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510dd6065899f34e92a17b88db1cb1ce4b9130bcd36f87ff97a9cfc7cd2430b8`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 19.2 MB (19165660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803567d33d1c34c1f24b0f2ca1c14b4b236cc528d23d4b4e2cd31a71d2d95cf9`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640dbcafae79da65d205c76809ffb4d36184629f730bbfe5390d61bdbb9bb592`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac5cd38945045e3390b31fbbf1b98016e77d70bfc1c8e4943c8a511454f46be`  
		Last Modified: Tue, 15 Apr 2025 22:14:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:15fb8f2e8e3351a29332a9e5dc5bc0e16656534be3ab802a11caa1460a38529a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86df0fb2d6368f9e61802919f3f8c0eabb1d0701f8e72287b61c2b8f28c25efd`

```dockerfile
```

-	Layers:
	-	`sha256:5d4936c9d50b732e7f62e0cc351a434d0368852afd6a10fb3311ec1be1a766dd`  
		Last Modified: Tue, 15 Apr 2025 22:14:26 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:4de6a5668da5d138bf9c18b29d2702e43c8773daee085087ba4fac61a6d34b7f
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
$ docker pull docker@sha256:9fb175225e8d3ff95ec41225424d3dcacf78af96544fb2aa2613a78a6d044cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140804349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26e595cb1df199dc05758e494ee8e1aa36bbd2c66b1e203108308187632b9fd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf07815168db14b53eefbc2c3049e107436cd426ee5b782a58f5dc0ce721611`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 8.1 MB (8062915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254bf878645b22853e806a0cb032d9e31d7d1e2fb63fa14996f2997754c4cc1`  
		Last Modified: Tue, 15 Apr 2025 21:57:55 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9c03f587febd06f516e8f5db9bfddcc26cfcb2e46713cd8964afe2cfa28e59`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 19.5 MB (19543064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8295a4327cea935c4c7193578b26fa033a39406088c826cd2d2cfe0f6341`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 21.5 MB (21456665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e931d098a4300b460baecb7bcd9871f0ac28ef04383131312e02105be2a254`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 20.9 MB (20915274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded655ab0883de9cda884f991c3ad2cb6ad71c325da540960fafd7ac2fe3bc5d`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa871cc6f3a41b34ac7bbbf20622b7983dd7eca584ee9afb54b2c8a04e664b9c`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c07c6b0cd3b4ba10c399f3467fd19017a58af5745b971b65c649d678609ce`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f314ec54f4e87b9fdd041baf54da645d0ddf3da9b65fac9f28b0b8c0a461abe`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 6.7 MB (6733013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62802569a7de6fb03151c263562da930e1286fb0532074c74e81abcdfd8c0844`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb73a7dab2ddd6d77007e093ca25de304da091667ee2ceed1d01602287dc96f`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b949978249f4df524390327d0a22df6fbbd2e120040d3496ad9cf7a7e33e68`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 60.4 MB (60352738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104b222ae0f025187b7161d740d6bbc959ea42706a47cf8f9992609b90b0a15`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edee73960c7ecf182956111c4e412314235d1bf7de03c03fb193a66cbb3b805a`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e9e881fce74013b8bd253845a1123f308d6f43a95f998e5fbcbc2b2a21350efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfc677921894b8bb22e951faa9c6358b561bd410a5a7bf854ea41fdad6ffcf9`

```dockerfile
```

-	Layers:
	-	`sha256:c5b5f23ce5548836116224bb8276806baaa70805aef357537f0c4af866495130`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:53f4029bd5c29e8412956b6a1168de2911e346048db80e9fe36ead17aaa351e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131459597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4dc168e6991627d0696aa634bdd8592b0e0cdc73c003058b3c97501c6085af`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb5ac7b586d2e616a3738487da728728e6ab907dbb55ca806bdbb258bffd4c`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 20.1 MB (20075447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cdba92e4820b290f335e99cc2497c15690be024cf49bfb3e84dae1d3b2f7aa`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 19.7 MB (19668391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f5df8cea3ca65fc59997f2930cee95224e394d2a822ef8fc86c93bc89a42b`  
		Last Modified: Tue, 15 Apr 2025 22:02:04 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd02c5d1daa4616ef9477cdfaf2938c59e4530da64323973c74114d1915a0e8`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784c0d09c497636b078403d01ba86ee45f69ea138e4c38778053cf12831fa589`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6385212aef435bf5fe83c846e5b0f0101cda8a2c35c997d5174641d636035133`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 7.0 MB (7036907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea41391ed39ae4550f757b7a9c4e6e7f72e03a2c84684b9b3af34a3982f0a6b`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 89.9 KB (89855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db336116a24939a7cb10bdd17233d99717160d5a44e329abcb3e1ea5133961a`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c90b7ec9b1e813885cf5d27bf57ec4ab9e7b12f2540f8099f75816b3eee94a`  
		Last Modified: Tue, 15 Apr 2025 22:30:06 GMT  
		Size: 55.7 MB (55741232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9694034f73e287b4e5985ba304e8f73b91060235fbc5598420119799e5464b`  
		Last Modified: Tue, 15 Apr 2025 22:30:05 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf9e7a6fda7047908acb8fca091d9b34be94912a469241a40168f9b789173b`  
		Last Modified: Tue, 15 Apr 2025 22:30:05 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:ba0d9764ae8f75d50f2ea82d950d8295c73ead10541e01d067eb22e4a9894ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52accc0ef60bca4959d92961236c8a7ed81d62a5855d8f91c662a056a8883f06`

```dockerfile
```

-	Layers:
	-	`sha256:19cf11c2a0717b5ca0dd4ab85a6d76e16f7c97b7e2bc73a1d63dd6a4a3c35d91`  
		Last Modified: Tue, 15 Apr 2025 22:30:03 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:2a2e09e827036692beebf4895f76b70ec7107429023bff61dc7e5e4fe13d783c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129795129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282a95b1fcf27a6134f8c92af53d356745663a43fe2972b5db8b40c4dd6934c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a864060af87a5048c5c602ac87964067948691631141ffc3818333edb16ed6`  
		Last Modified: Tue, 15 Apr 2025 22:13:41 GMT  
		Size: 7.3 MB (7301755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c418fb5b9eb8648b75bfdc32d3b64717b14e09489dfedf7e46fc76341ad53`  
		Last Modified: Tue, 15 Apr 2025 22:13:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd85b047c7948100b1f2399a8eea9d8b0b88f7e5be1fb7dc2dafae83f9abc79`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 17.5 MB (17486305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260399ab5d107c45411de9a9bb80ceb98c4127d21afb7d74f09f28159a401c37`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 20.1 MB (20055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac89693fff3745a0f965eeb714910187ffa11d066e9350cd739ac8abd51851`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 19.7 MB (19651336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d180cbaf95968e95d53d1e91cebf8edb96d048a9cf7d70de617dbf1fc294ea7`  
		Last Modified: Tue, 15 Apr 2025 22:14:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0055fbe8376d2bdc3df4d623bcc98e03e488ca7d5b016ad04967401ad02deb`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac853fc592a73bec02462f288dccaffe3e3a3d6df3674ffeac7fc1700698529d`  
		Last Modified: Tue, 15 Apr 2025 22:14:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5184d90f6369c2f5f1e29a37fe3b3fb3e0539b04e800513c8a853d38c650499`  
		Last Modified: Tue, 15 Apr 2025 22:35:10 GMT  
		Size: 6.4 MB (6366053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1acf458da982581dd9b61a4a0956dbee6993e62bba3116184a25fe59a3f733`  
		Last Modified: Tue, 15 Apr 2025 22:35:09 GMT  
		Size: 86.4 KB (86361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c270a2cf682f8879277f147121c3e5d87771a05bc795d9d59f2a6db996a452af`  
		Last Modified: Tue, 15 Apr 2025 22:35:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e7bcdf843369eb576f5159861f0097b833abb7c49fd377711ce5939a7b1de`  
		Last Modified: Tue, 15 Apr 2025 22:35:12 GMT  
		Size: 55.7 MB (55741239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b943e454e66f65972d76e9082ba248befda3168ed13b26a4cbc36e27b35744`  
		Last Modified: Tue, 15 Apr 2025 22:35:11 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753779b323550f5a1e0443228843cf7835bc5d6f2fbd8d1ce67047cebcbae09f`  
		Last Modified: Tue, 15 Apr 2025 22:35:11 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a0623b4bb16f8485ecdbe795429d3dd4719d250ce0882e82931a6320968e5af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1e2701fe2f97efe7673d949bf676ad4f5eb2da5c330f6e5d4e15815a241d88`

```dockerfile
```

-	Layers:
	-	`sha256:b21d7fb3b31d9e2a5468fc38c926984d475bf91cefe7ab9bd350a7de9119b091`  
		Last Modified: Tue, 15 Apr 2025 22:35:09 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5d4d2e49343b6e3788b1b9dfa0e6510e5787ede7a75621a8eb61dfb409748797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132182786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969af15cd525f0961932384442d28f48239790e80f2ef068806c0cd05b58d192`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e41a332ac34c555abfc416477e260fbde6301802d8e137957166d7b7269e14`  
		Last Modified: Tue, 15 Apr 2025 22:05:00 GMT  
		Size: 8.1 MB (8077251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b44bc2c49279b62c624fcbb004d6fb2af3e11e622deceb7b73b2d962d7213`  
		Last Modified: Tue, 15 Apr 2025 22:04:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548b10c496662caab533c3d131758d622285b3f373756838531f1a168224831`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 18.5 MB (18457152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a45d6fe346d03b0272285dd9725e00aefad8b06d1f295635b39c9630cc6a6`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 19.7 MB (19692478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510dd6065899f34e92a17b88db1cb1ce4b9130bcd36f87ff97a9cfc7cd2430b8`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 19.2 MB (19165660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803567d33d1c34c1f24b0f2ca1c14b4b236cc528d23d4b4e2cd31a71d2d95cf9`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640dbcafae79da65d205c76809ffb4d36184629f730bbfe5390d61bdbb9bb592`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac5cd38945045e3390b31fbbf1b98016e77d70bfc1c8e4943c8a511454f46be`  
		Last Modified: Tue, 15 Apr 2025 22:14:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dc6d9cc98ef412cebe1089c79a0b32ddfed7b3321d6fa49c3b1d7dbe4b3c70`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a9f3b4322221600837bd19350617e9fbdf944b0f97ea579f4969f6e5d6049e`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 99.4 KB (99378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60eb0dce1bf078d608f862da78405ed0a6787825fbd8f9584b22f503dab449c`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ed7a6d0e2d072bf5c0d02797956e1062a2c902e2aab07367bdfe977c466161`  
		Last Modified: Tue, 15 Apr 2025 22:26:03 GMT  
		Size: 55.7 MB (55710879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1e30286ee5a0c6035e171d60a2b4e64cceaf5e8d3b4b7744f47a2c3affcc0`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180e29b0ef2ab0fe57327b9d65d69b7d92b6245d338b4a9eaf59353772f325e`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:704d76da08f415078565b0728f7e1a80695fd64414e71af349d8bbc76e7b85d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3d917794b140e94e3032fe9ad8f6d1045f397961d2a8ef17c4bc86318782f8`

```dockerfile
```

-	Layers:
	-	`sha256:97e71ce1d2497e5c4723f68f9b66746699cc08da3d199b87ca3346f8aa33fa12`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:b657df8f8aad102f8bc05908deb58402ec791eeffe7b4470e5d576f0e6743765
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:54db6d9791dffefd0b528527b4ed346ae1135a7a05aa8e6da053c1f07314087e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158963462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67318ae1c4af8b4ee0f8bfee72355afe97fb8edaca0fc9265a4ff060b4e0ca3a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf07815168db14b53eefbc2c3049e107436cd426ee5b782a58f5dc0ce721611`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 8.1 MB (8062915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254bf878645b22853e806a0cb032d9e31d7d1e2fb63fa14996f2997754c4cc1`  
		Last Modified: Tue, 15 Apr 2025 21:57:55 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9c03f587febd06f516e8f5db9bfddcc26cfcb2e46713cd8964afe2cfa28e59`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 19.5 MB (19543064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8295a4327cea935c4c7193578b26fa033a39406088c826cd2d2cfe0f6341`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 21.5 MB (21456665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e931d098a4300b460baecb7bcd9871f0ac28ef04383131312e02105be2a254`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 20.9 MB (20915274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded655ab0883de9cda884f991c3ad2cb6ad71c325da540960fafd7ac2fe3bc5d`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa871cc6f3a41b34ac7bbbf20622b7983dd7eca584ee9afb54b2c8a04e664b9c`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c07c6b0cd3b4ba10c399f3467fd19017a58af5745b971b65c649d678609ce`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f314ec54f4e87b9fdd041baf54da645d0ddf3da9b65fac9f28b0b8c0a461abe`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 6.7 MB (6733013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62802569a7de6fb03151c263562da930e1286fb0532074c74e81abcdfd8c0844`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb73a7dab2ddd6d77007e093ca25de304da091667ee2ceed1d01602287dc96f`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b949978249f4df524390327d0a22df6fbbd2e120040d3496ad9cf7a7e33e68`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 60.4 MB (60352738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104b222ae0f025187b7161d740d6bbc959ea42706a47cf8f9992609b90b0a15`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edee73960c7ecf182956111c4e412314235d1bf7de03c03fb193a66cbb3b805a`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbcaf9af1c4542b39548057db3f89ae883e4e42939e64d7809846eed60d4901`  
		Last Modified: Tue, 15 Apr 2025 22:07:45 GMT  
		Size: 986.6 KB (986581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5afaf14a7ec7e06da772bfe38b6f176ff48c453aa74c27de975da807227f52`  
		Last Modified: Tue, 15 Apr 2025 22:07:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdb8f0bdf277c33789ad7e6bb8fce62ba7dd2c92b55e56b0dd61bbd48cc6c1f`  
		Last Modified: Tue, 15 Apr 2025 22:07:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318db3731ff5e1712ab1830de247b8de7a02438f87fcacc4f38fa130f07e2d2a`  
		Last Modified: Tue, 15 Apr 2025 22:07:46 GMT  
		Size: 17.2 MB (17171190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78277d8b957a21553e462b53bbdafb59e66dd775c13421cf61a32a2018941610`  
		Last Modified: Tue, 15 Apr 2025 22:07:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:18aebec3500d96ffee670ca9cf9d842f9123222ce6f5231e4495502266c16c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff35a275e95e551cee5b91de19401fccefa589d3449daee2aafcbfd59fe8df5c`

```dockerfile
```

-	Layers:
	-	`sha256:4a83080acbcd380cf2c01a825d8a390ff7cf4b9c2f4ea899b691d728c0edeaa1`  
		Last Modified: Tue, 15 Apr 2025 22:07:45 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1ff1b98f479dc58cfed04fb991acff688f27a33361568286d93f4b2bf7c43acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152480473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83441b3def8697388a05af1983ee55c6a63d6b2d35756fd153f06c58041d6aec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e41a332ac34c555abfc416477e260fbde6301802d8e137957166d7b7269e14`  
		Last Modified: Tue, 15 Apr 2025 22:05:00 GMT  
		Size: 8.1 MB (8077251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b44bc2c49279b62c624fcbb004d6fb2af3e11e622deceb7b73b2d962d7213`  
		Last Modified: Tue, 15 Apr 2025 22:04:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548b10c496662caab533c3d131758d622285b3f373756838531f1a168224831`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 18.5 MB (18457152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a45d6fe346d03b0272285dd9725e00aefad8b06d1f295635b39c9630cc6a6`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 19.7 MB (19692478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510dd6065899f34e92a17b88db1cb1ce4b9130bcd36f87ff97a9cfc7cd2430b8`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 19.2 MB (19165660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803567d33d1c34c1f24b0f2ca1c14b4b236cc528d23d4b4e2cd31a71d2d95cf9`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640dbcafae79da65d205c76809ffb4d36184629f730bbfe5390d61bdbb9bb592`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac5cd38945045e3390b31fbbf1b98016e77d70bfc1c8e4943c8a511454f46be`  
		Last Modified: Tue, 15 Apr 2025 22:14:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dc6d9cc98ef412cebe1089c79a0b32ddfed7b3321d6fa49c3b1d7dbe4b3c70`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a9f3b4322221600837bd19350617e9fbdf944b0f97ea579f4969f6e5d6049e`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 99.4 KB (99378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60eb0dce1bf078d608f862da78405ed0a6787825fbd8f9584b22f503dab449c`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ed7a6d0e2d072bf5c0d02797956e1062a2c902e2aab07367bdfe977c466161`  
		Last Modified: Tue, 15 Apr 2025 22:26:03 GMT  
		Size: 55.7 MB (55710879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1e30286ee5a0c6035e171d60a2b4e64cceaf5e8d3b4b7744f47a2c3affcc0`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180e29b0ef2ab0fe57327b9d65d69b7d92b6245d338b4a9eaf59353772f325e`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593538725234e7f5471d5edcd1545b428c2be3e765746760f8fbaea46b2965a9`  
		Last Modified: Tue, 15 Apr 2025 23:07:21 GMT  
		Size: 1.0 MB (1014211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f87db4b1a10e689b727a320ef2869a263d4e8c3dc046cd0976435e2d34d983`  
		Last Modified: Tue, 15 Apr 2025 23:07:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48c5275d28148d3c58af76a48d45befc03d686c8647f4569a07da472d3fb932`  
		Last Modified: Tue, 15 Apr 2025 23:07:21 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f1b4eeca171dd968721ebed2f30758cc913ca1fc968d32aaec90b0e4501fc0`  
		Last Modified: Tue, 15 Apr 2025 23:07:22 GMT  
		Size: 19.3 MB (19282132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19c98b4578bd75541d368745c684355023aeed914370664c16ce434016cefa6`  
		Last Modified: Tue, 15 Apr 2025 23:07:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:de3d621c088272cc86d5c7777395aceab3af8e685ee6605b4f4011e6b8f02f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724e2934dbdc120f6444a7c1e06fb77a2ebb3194079761af1ea85196deb8f8c6`

```dockerfile
```

-	Layers:
	-	`sha256:6afe9376f42157faae689cdd015195db7c251375305753dc292b96e889342beb`  
		Last Modified: Tue, 15 Apr 2025 23:07:20 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:4de6a5668da5d138bf9c18b29d2702e43c8773daee085087ba4fac61a6d34b7f
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
$ docker pull docker@sha256:9fb175225e8d3ff95ec41225424d3dcacf78af96544fb2aa2613a78a6d044cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140804349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26e595cb1df199dc05758e494ee8e1aa36bbd2c66b1e203108308187632b9fd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf07815168db14b53eefbc2c3049e107436cd426ee5b782a58f5dc0ce721611`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 8.1 MB (8062915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254bf878645b22853e806a0cb032d9e31d7d1e2fb63fa14996f2997754c4cc1`  
		Last Modified: Tue, 15 Apr 2025 21:57:55 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9c03f587febd06f516e8f5db9bfddcc26cfcb2e46713cd8964afe2cfa28e59`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 19.5 MB (19543064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8295a4327cea935c4c7193578b26fa033a39406088c826cd2d2cfe0f6341`  
		Last Modified: Tue, 15 Apr 2025 21:57:56 GMT  
		Size: 21.5 MB (21456665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e931d098a4300b460baecb7bcd9871f0ac28ef04383131312e02105be2a254`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 20.9 MB (20915274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded655ab0883de9cda884f991c3ad2cb6ad71c325da540960fafd7ac2fe3bc5d`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa871cc6f3a41b34ac7bbbf20622b7983dd7eca584ee9afb54b2c8a04e664b9c`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c07c6b0cd3b4ba10c399f3467fd19017a58af5745b971b65c649d678609ce`  
		Last Modified: Tue, 15 Apr 2025 21:57:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f314ec54f4e87b9fdd041baf54da645d0ddf3da9b65fac9f28b0b8c0a461abe`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 6.7 MB (6733013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62802569a7de6fb03151c263562da930e1286fb0532074c74e81abcdfd8c0844`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb73a7dab2ddd6d77007e093ca25de304da091667ee2ceed1d01602287dc96f`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b949978249f4df524390327d0a22df6fbbd2e120040d3496ad9cf7a7e33e68`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 60.4 MB (60352738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104b222ae0f025187b7161d740d6bbc959ea42706a47cf8f9992609b90b0a15`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edee73960c7ecf182956111c4e412314235d1bf7de03c03fb193a66cbb3b805a`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:e9e881fce74013b8bd253845a1123f308d6f43a95f998e5fbcbc2b2a21350efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfc677921894b8bb22e951faa9c6358b561bd410a5a7bf854ea41fdad6ffcf9`

```dockerfile
```

-	Layers:
	-	`sha256:c5b5f23ce5548836116224bb8276806baaa70805aef357537f0c4af866495130`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:53f4029bd5c29e8412956b6a1168de2911e346048db80e9fe36ead17aaa351e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131459597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4dc168e6991627d0696aa634bdd8592b0e0cdc73c003058b3c97501c6085af`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb5ac7b586d2e616a3738487da728728e6ab907dbb55ca806bdbb258bffd4c`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 20.1 MB (20075447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cdba92e4820b290f335e99cc2497c15690be024cf49bfb3e84dae1d3b2f7aa`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 19.7 MB (19668391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f5df8cea3ca65fc59997f2930cee95224e394d2a822ef8fc86c93bc89a42b`  
		Last Modified: Tue, 15 Apr 2025 22:02:04 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd02c5d1daa4616ef9477cdfaf2938c59e4530da64323973c74114d1915a0e8`  
		Last Modified: Tue, 15 Apr 2025 22:02:05 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784c0d09c497636b078403d01ba86ee45f69ea138e4c38778053cf12831fa589`  
		Last Modified: Tue, 15 Apr 2025 22:02:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6385212aef435bf5fe83c846e5b0f0101cda8a2c35c997d5174641d636035133`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 7.0 MB (7036907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea41391ed39ae4550f757b7a9c4e6e7f72e03a2c84684b9b3af34a3982f0a6b`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 89.9 KB (89855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db336116a24939a7cb10bdd17233d99717160d5a44e329abcb3e1ea5133961a`  
		Last Modified: Tue, 15 Apr 2025 22:30:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c90b7ec9b1e813885cf5d27bf57ec4ab9e7b12f2540f8099f75816b3eee94a`  
		Last Modified: Tue, 15 Apr 2025 22:30:06 GMT  
		Size: 55.7 MB (55741232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9694034f73e287b4e5985ba304e8f73b91060235fbc5598420119799e5464b`  
		Last Modified: Tue, 15 Apr 2025 22:30:05 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf9e7a6fda7047908acb8fca091d9b34be94912a469241a40168f9b789173b`  
		Last Modified: Tue, 15 Apr 2025 22:30:05 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:ba0d9764ae8f75d50f2ea82d950d8295c73ead10541e01d067eb22e4a9894ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52accc0ef60bca4959d92961236c8a7ed81d62a5855d8f91c662a056a8883f06`

```dockerfile
```

-	Layers:
	-	`sha256:19cf11c2a0717b5ca0dd4ab85a6d76e16f7c97b7e2bc73a1d63dd6a4a3c35d91`  
		Last Modified: Tue, 15 Apr 2025 22:30:03 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:2a2e09e827036692beebf4895f76b70ec7107429023bff61dc7e5e4fe13d783c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129795129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282a95b1fcf27a6134f8c92af53d356745663a43fe2972b5db8b40c4dd6934c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a864060af87a5048c5c602ac87964067948691631141ffc3818333edb16ed6`  
		Last Modified: Tue, 15 Apr 2025 22:13:41 GMT  
		Size: 7.3 MB (7301755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c418fb5b9eb8648b75bfdc32d3b64717b14e09489dfedf7e46fc76341ad53`  
		Last Modified: Tue, 15 Apr 2025 22:13:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd85b047c7948100b1f2399a8eea9d8b0b88f7e5be1fb7dc2dafae83f9abc79`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 17.5 MB (17486305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260399ab5d107c45411de9a9bb80ceb98c4127d21afb7d74f09f28159a401c37`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 20.1 MB (20055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac89693fff3745a0f965eeb714910187ffa11d066e9350cd739ac8abd51851`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 19.7 MB (19651336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d180cbaf95968e95d53d1e91cebf8edb96d048a9cf7d70de617dbf1fc294ea7`  
		Last Modified: Tue, 15 Apr 2025 22:14:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0055fbe8376d2bdc3df4d623bcc98e03e488ca7d5b016ad04967401ad02deb`  
		Last Modified: Tue, 15 Apr 2025 22:14:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac853fc592a73bec02462f288dccaffe3e3a3d6df3674ffeac7fc1700698529d`  
		Last Modified: Tue, 15 Apr 2025 22:14:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5184d90f6369c2f5f1e29a37fe3b3fb3e0539b04e800513c8a853d38c650499`  
		Last Modified: Tue, 15 Apr 2025 22:35:10 GMT  
		Size: 6.4 MB (6366053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1acf458da982581dd9b61a4a0956dbee6993e62bba3116184a25fe59a3f733`  
		Last Modified: Tue, 15 Apr 2025 22:35:09 GMT  
		Size: 86.4 KB (86361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c270a2cf682f8879277f147121c3e5d87771a05bc795d9d59f2a6db996a452af`  
		Last Modified: Tue, 15 Apr 2025 22:35:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e7bcdf843369eb576f5159861f0097b833abb7c49fd377711ce5939a7b1de`  
		Last Modified: Tue, 15 Apr 2025 22:35:12 GMT  
		Size: 55.7 MB (55741239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b943e454e66f65972d76e9082ba248befda3168ed13b26a4cbc36e27b35744`  
		Last Modified: Tue, 15 Apr 2025 22:35:11 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753779b323550f5a1e0443228843cf7835bc5d6f2fbd8d1ce67047cebcbae09f`  
		Last Modified: Tue, 15 Apr 2025 22:35:11 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a0623b4bb16f8485ecdbe795429d3dd4719d250ce0882e82931a6320968e5af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1e2701fe2f97efe7673d949bf676ad4f5eb2da5c330f6e5d4e15815a241d88`

```dockerfile
```

-	Layers:
	-	`sha256:b21d7fb3b31d9e2a5468fc38c926984d475bf91cefe7ab9bd350a7de9119b091`  
		Last Modified: Tue, 15 Apr 2025 22:35:09 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5d4d2e49343b6e3788b1b9dfa0e6510e5787ede7a75621a8eb61dfb409748797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132182786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969af15cd525f0961932384442d28f48239790e80f2ef068806c0cd05b58d192`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e41a332ac34c555abfc416477e260fbde6301802d8e137957166d7b7269e14`  
		Last Modified: Tue, 15 Apr 2025 22:05:00 GMT  
		Size: 8.1 MB (8077251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b44bc2c49279b62c624fcbb004d6fb2af3e11e622deceb7b73b2d962d7213`  
		Last Modified: Tue, 15 Apr 2025 22:04:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548b10c496662caab533c3d131758d622285b3f373756838531f1a168224831`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 18.5 MB (18457152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a45d6fe346d03b0272285dd9725e00aefad8b06d1f295635b39c9630cc6a6`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 19.7 MB (19692478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510dd6065899f34e92a17b88db1cb1ce4b9130bcd36f87ff97a9cfc7cd2430b8`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 19.2 MB (19165660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803567d33d1c34c1f24b0f2ca1c14b4b236cc528d23d4b4e2cd31a71d2d95cf9`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640dbcafae79da65d205c76809ffb4d36184629f730bbfe5390d61bdbb9bb592`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac5cd38945045e3390b31fbbf1b98016e77d70bfc1c8e4943c8a511454f46be`  
		Last Modified: Tue, 15 Apr 2025 22:14:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dc6d9cc98ef412cebe1089c79a0b32ddfed7b3321d6fa49c3b1d7dbe4b3c70`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a9f3b4322221600837bd19350617e9fbdf944b0f97ea579f4969f6e5d6049e`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 99.4 KB (99378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60eb0dce1bf078d608f862da78405ed0a6787825fbd8f9584b22f503dab449c`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ed7a6d0e2d072bf5c0d02797956e1062a2c902e2aab07367bdfe977c466161`  
		Last Modified: Tue, 15 Apr 2025 22:26:03 GMT  
		Size: 55.7 MB (55710879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1e30286ee5a0c6035e171d60a2b4e64cceaf5e8d3b4b7744f47a2c3affcc0`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180e29b0ef2ab0fe57327b9d65d69b7d92b6245d338b4a9eaf59353772f325e`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:704d76da08f415078565b0728f7e1a80695fd64414e71af349d8bbc76e7b85d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3d917794b140e94e3032fe9ad8f6d1045f397961d2a8ef17c4bc86318782f8`

```dockerfile
```

-	Layers:
	-	`sha256:97e71ce1d2497e5c4723f68f9b66746699cc08da3d199b87ca3346f8aa33fa12`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:528a394441b948ca8fa2ccce01b95f52233729ab27342fb1aa0339e63eac858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8aa47cd924b443e6ed4f2293a2350df34e37e3840d7f2d10fa31ee848767b822
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459291937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554c35c4d3f914e6695b9b090d2e9d3f4038ed0707cc2979c1a8536f166c3b58`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Tue, 15 Apr 2025 22:05:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:05:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:05:42 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:05:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:06:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:06:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:06:31 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:06:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:07:24 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:08:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff803ad22e0ab64f102a722831537db638cc47772e62fa4f66ffc6a1de17bea`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650f48f4339554104a9b685c62ece86c0131ae6c202350e5f1a52e3a37ce006`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 405.2 KB (405161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc49ea6a08f7cb24b63b58139a6dd7d541e4be2c493b13edb6baeadc60ec9d`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d558fa4719a5fac8b7e21cdb0c03d7fb86edd8d43dc1def3abb70c02fcb75805`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148fc3d5ca192103ee3ae1835ce8a09f63c602ef431fcd5e749aa31c35237cdc`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 19.9 MB (19909526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71983d7eafa2374ca5c49782e81dfe35e5039870e7cd99abd2974726f1abdda7`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f2a4a7cef42383900d86e61ce89a2cc511ce078fbd6ef543452b57decc48f6`  
		Last Modified: Tue, 15 Apr 2025 22:08:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb3b7cf9449e0a48b9b27cc9b0f6deece3b5fbe51dd4f277c9570e360b2184f`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb088745c9e5fe660fc7a745b3a9a54607c55d7bae09a18c30a152001e325528`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 22.4 MB (22401686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90041ef92672e9384ec94e0d96df6bb0002534b8aeefcfb5a4d714743ef3706f`  
		Last Modified: Tue, 15 Apr 2025 22:08:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70fc9c300e4e7129f577f4f0812ba764164930ed15018563351f6be609e05d5`  
		Last Modified: Tue, 15 Apr 2025 22:08:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efa5c78927c877cdbd1b451ae71d849f427bfdc3c04a356a4c4bb65152dc2d4`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c4122ecb346154069beaab3457ca61e4629a9de2c32cbeb64f92387e9c96a2`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 21.9 MB (21884365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:68e38ab953a87c61b66914217106b383daee357c4c05b1647ab3a95bfe7d79ce
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335455807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbf36de339df80f34209544c9b63f8b7d83ca23f9337314dfe2eaf417fd644b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Tue, 15 Apr 2025 22:07:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:07:48 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:07:49 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:07:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:07:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:08:00 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:08:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:08:01 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:08:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:08:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:08:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:08:10 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:08:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30151e3643fba377542afac5a171a0527fd990206b8e89128562f09c6b6f761f`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4725ce2acf24e3219acaaa964606e83f8b4a7f2ff49c13f3261a641951a8b1db`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 365.7 KB (365726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9b91c0fe3a715c4879fa6fff556bfc191f884bdcdf19bbdbac4be05eab6fd`  
		Last Modified: Tue, 15 Apr 2025 22:08:25 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919b934268d7cf70b58919f0e50f2a45315bff20b5f9b7e83faca5460b955586`  
		Last Modified: Tue, 15 Apr 2025 22:08:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6737480d00e37347bf879f9271d4ebf5445bd23e5631768e209d02fabc332cf5`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 19.9 MB (19871309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbdcff4db952a6d899885eb2d490f38cc558e145ddd9895b34fdd6d7f8e7c87`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c7b3a352e7efdbbbb5c2e6eeea9ed5deb2f375780a083421b2a6d863238125`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45f0f2eb53c4197068fb31b358a34a63517e22eef46f899066d3417c1f86c05`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07362729c8326851ce50b1c80ca2976934c0ccdee6a27216870ecc812ea693de`  
		Last Modified: Tue, 15 Apr 2025 22:08:24 GMT  
		Size: 22.4 MB (22364101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c09098cac7c45c8f6f1cf5d8e638a25be610c8efd36fe246f0cf0097b1bfde1`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ceaf713f2cf3069d80077b0c0dce7dd6b385d96f318a7fd5b600daf6953008d`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef372443d99cb8ae017ed4b09096ce301d468ff7d48f33711ffa40177c21a85`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc61b0ba2c5210eb8100bc7189348241ae40e963445358cf48edf32774055787`  
		Last Modified: Tue, 15 Apr 2025 22:08:24 GMT  
		Size: 21.8 MB (21847429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:9eea48e8624f5a89b632b349df9a9ef60250b1c5ffa205d3d91cf43c32846ccd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227127342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785c3dec269da97ebda3793c1818235279080fd52a121be171f0b57b16ddba27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Tue, 15 Apr 2025 22:12:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:13:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:13:23 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:13:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:13:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:39 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:13:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:13:41 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:13:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:14:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75559a6ab4985605769e9345e4dff1b1dcce036c5e3f010989bc5d815bcf22db`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbc5225e1556802cd30f8fd34e34314e3d8b61a8646572689a40d59b303a269`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 341.5 KB (341494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5c9f84290e2fafec5927a5d6d17a3a064c93078c593270106ea74ad23ec29a`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bcf429ac4797944cc945ce64dc94e477c8d14341b6fecaf29b9ccc44180cb2`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a44bd61aef7b941f7614c31fb50b8660886b2740bbb23a09d281aef1f08832b`  
		Last Modified: Tue, 15 Apr 2025 22:14:11 GMT  
		Size: 19.9 MB (19860556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d18acc9d9a4944f4b68e2eb3b2056dc918d4f3155a9de9469b804883c9a870`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9fb93169fb4009bfe58fef0cb707780bf6d1452c6b71e4add92e8c230fd923`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d2981dd79b2395c71b1f2abf10aa7e31aafcd81b94c306767eb6394e5caf23`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a04a74dc2f144ff9e196e62a1c06e6277d5004443ce5b7de37e0d4aaa59a13b`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 22.4 MB (22354530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d80f4121c811468ee950acee266056e1e05a0e7ed4750dba28b1290f9444c9`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86e7151feda14da9b65f7fa4811a3d9f596a3f632eee42ca1a9173930178878`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62c931e923807455c87709bcd05a0d7067b18b8f1033c6fc5bb4f1d77c0d98b`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a55036ef8e12942d5bc9f5782020380597b798bdec106fbd29daa958030524`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 21.8 MB (21833195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:6fed54b785c39f7c584b70ac3c8ff8859e0f3517dcc298ea0f3bebcf7e205572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:9eea48e8624f5a89b632b349df9a9ef60250b1c5ffa205d3d91cf43c32846ccd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227127342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785c3dec269da97ebda3793c1818235279080fd52a121be171f0b57b16ddba27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Tue, 15 Apr 2025 22:12:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:13:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:13:23 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:13:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:13:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:39 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:13:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:13:41 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:13:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:14:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75559a6ab4985605769e9345e4dff1b1dcce036c5e3f010989bc5d815bcf22db`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbc5225e1556802cd30f8fd34e34314e3d8b61a8646572689a40d59b303a269`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 341.5 KB (341494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5c9f84290e2fafec5927a5d6d17a3a064c93078c593270106ea74ad23ec29a`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bcf429ac4797944cc945ce64dc94e477c8d14341b6fecaf29b9ccc44180cb2`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a44bd61aef7b941f7614c31fb50b8660886b2740bbb23a09d281aef1f08832b`  
		Last Modified: Tue, 15 Apr 2025 22:14:11 GMT  
		Size: 19.9 MB (19860556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d18acc9d9a4944f4b68e2eb3b2056dc918d4f3155a9de9469b804883c9a870`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9fb93169fb4009bfe58fef0cb707780bf6d1452c6b71e4add92e8c230fd923`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d2981dd79b2395c71b1f2abf10aa7e31aafcd81b94c306767eb6394e5caf23`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a04a74dc2f144ff9e196e62a1c06e6277d5004443ce5b7de37e0d4aaa59a13b`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 22.4 MB (22354530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d80f4121c811468ee950acee266056e1e05a0e7ed4750dba28b1290f9444c9`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86e7151feda14da9b65f7fa4811a3d9f596a3f632eee42ca1a9173930178878`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62c931e923807455c87709bcd05a0d7067b18b8f1033c6fc5bb4f1d77c0d98b`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a55036ef8e12942d5bc9f5782020380597b798bdec106fbd29daa958030524`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 21.8 MB (21833195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:01607c0fe392d1b599a20ff0eaa2cb95b736b9178f561477ca918103bb8d1d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:68e38ab953a87c61b66914217106b383daee357c4c05b1647ab3a95bfe7d79ce
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335455807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbf36de339df80f34209544c9b63f8b7d83ca23f9337314dfe2eaf417fd644b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Tue, 15 Apr 2025 22:07:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:07:48 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:07:49 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:07:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:07:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:08:00 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:08:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:08:01 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:08:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:08:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:08:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:08:10 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:08:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30151e3643fba377542afac5a171a0527fd990206b8e89128562f09c6b6f761f`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4725ce2acf24e3219acaaa964606e83f8b4a7f2ff49c13f3261a641951a8b1db`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 365.7 KB (365726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9b91c0fe3a715c4879fa6fff556bfc191f884bdcdf19bbdbac4be05eab6fd`  
		Last Modified: Tue, 15 Apr 2025 22:08:25 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919b934268d7cf70b58919f0e50f2a45315bff20b5f9b7e83faca5460b955586`  
		Last Modified: Tue, 15 Apr 2025 22:08:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6737480d00e37347bf879f9271d4ebf5445bd23e5631768e209d02fabc332cf5`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 19.9 MB (19871309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbdcff4db952a6d899885eb2d490f38cc558e145ddd9895b34fdd6d7f8e7c87`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c7b3a352e7efdbbbb5c2e6eeea9ed5deb2f375780a083421b2a6d863238125`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45f0f2eb53c4197068fb31b358a34a63517e22eef46f899066d3417c1f86c05`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07362729c8326851ce50b1c80ca2976934c0ccdee6a27216870ecc812ea693de`  
		Last Modified: Tue, 15 Apr 2025 22:08:24 GMT  
		Size: 22.4 MB (22364101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c09098cac7c45c8f6f1cf5d8e638a25be610c8efd36fe246f0cf0097b1bfde1`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ceaf713f2cf3069d80077b0c0dce7dd6b385d96f318a7fd5b600daf6953008d`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef372443d99cb8ae017ed4b09096ce301d468ff7d48f33711ffa40177c21a85`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc61b0ba2c5210eb8100bc7189348241ae40e963445358cf48edf32774055787`  
		Last Modified: Tue, 15 Apr 2025 22:08:24 GMT  
		Size: 21.8 MB (21847429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:eaa298de788f906bf4dcaba103c3a6b9102985e0ba21d3c89c6523fd4b944435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8aa47cd924b443e6ed4f2293a2350df34e37e3840d7f2d10fa31ee848767b822
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459291937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554c35c4d3f914e6695b9b090d2e9d3f4038ed0707cc2979c1a8536f166c3b58`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Tue, 15 Apr 2025 22:05:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:05:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:05:42 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:05:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:06:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:06:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:06:31 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:06:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:07:24 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:08:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff803ad22e0ab64f102a722831537db638cc47772e62fa4f66ffc6a1de17bea`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650f48f4339554104a9b685c62ece86c0131ae6c202350e5f1a52e3a37ce006`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 405.2 KB (405161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc49ea6a08f7cb24b63b58139a6dd7d541e4be2c493b13edb6baeadc60ec9d`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d558fa4719a5fac8b7e21cdb0c03d7fb86edd8d43dc1def3abb70c02fcb75805`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148fc3d5ca192103ee3ae1835ce8a09f63c602ef431fcd5e749aa31c35237cdc`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 19.9 MB (19909526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71983d7eafa2374ca5c49782e81dfe35e5039870e7cd99abd2974726f1abdda7`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f2a4a7cef42383900d86e61ce89a2cc511ce078fbd6ef543452b57decc48f6`  
		Last Modified: Tue, 15 Apr 2025 22:08:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb3b7cf9449e0a48b9b27cc9b0f6deece3b5fbe51dd4f277c9570e360b2184f`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb088745c9e5fe660fc7a745b3a9a54607c55d7bae09a18c30a152001e325528`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 22.4 MB (22401686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90041ef92672e9384ec94e0d96df6bb0002534b8aeefcfb5a4d714743ef3706f`  
		Last Modified: Tue, 15 Apr 2025 22:08:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70fc9c300e4e7129f577f4f0812ba764164930ed15018563351f6be609e05d5`  
		Last Modified: Tue, 15 Apr 2025 22:08:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efa5c78927c877cdbd1b451ae71d849f427bfdc3c04a356a4c4bb65152dc2d4`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c4122ecb346154069beaab3457ca61e4629a9de2c32cbeb64f92387e9c96a2`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 21.9 MB (21884365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
