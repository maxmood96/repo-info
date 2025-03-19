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
-	[`docker:28.0`](#docker280)
-	[`docker:28.0-cli`](#docker280-cli)
-	[`docker:28.0-dind`](#docker280-dind)
-	[`docker:28.0-dind-rootless`](#docker280-dind-rootless)
-	[`docker:28.0-windowsservercore`](#docker280-windowsservercore)
-	[`docker:28.0-windowsservercore-1809`](#docker280-windowsservercore-1809)
-	[`docker:28.0-windowsservercore-ltsc2022`](#docker280-windowsservercore-ltsc2022)
-	[`docker:28.0-windowsservercore-ltsc2025`](#docker280-windowsservercore-ltsc2025)
-	[`docker:28.0.1`](#docker2801)
-	[`docker:28.0.1-alpine3.21`](#docker2801-alpine321)
-	[`docker:28.0.1-cli`](#docker2801-cli)
-	[`docker:28.0.1-cli-alpine3.21`](#docker2801-cli-alpine321)
-	[`docker:28.0.1-dind`](#docker2801-dind)
-	[`docker:28.0.1-dind-alpine3.21`](#docker2801-dind-alpine321)
-	[`docker:28.0.1-dind-rootless`](#docker2801-dind-rootless)
-	[`docker:28.0.1-windowsservercore`](#docker2801-windowsservercore)
-	[`docker:28.0.1-windowsservercore-1809`](#docker2801-windowsservercore-1809)
-	[`docker:28.0.1-windowsservercore-ltsc2022`](#docker2801-windowsservercore-ltsc2022)
-	[`docker:28.0.1-windowsservercore-ltsc2025`](#docker2801-windowsservercore-ltsc2025)
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
$ docker pull docker@sha256:828290aa6d563454a849d59ca1bdfb14804679fa96ac0ba8eeabd76ee73c145d
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
$ docker pull docker@sha256:6f284d567aabce6fc59489d515b32e9e9e3c434d56a30a5bb4c78e31f8ce4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141423867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ebdb25d1582b57307f7586f07df28009b8bfe0ccafff9ccf38d2ece7e6142d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:b14dff50fdd36d583da1a62ad48743534c80d36636deb306ef3ea726fcc631b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c0320c0a080ec3869c570d9dcd47939db272e83fe901841e581fddfb923ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff3751a52465c2f4ca6f364704b34afeadb9a193f007f86b91faabe58e430298`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:66ed15e7c3455a7bd74e92449060237f9e6cd0c4a930a26cd8a90d344b555c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132050936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3635197fd3d2349cbe43887a8904a6cedcff1a4671bba7cab1a281c3bdaa98b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a710f976bef50357a64879fea6e83351c1d0ef59c4b2e03ab5c02c7d00693a`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 7.0 MB (7036932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd6d7147ebc3737f9054c3a2e0840f16cffd6eeb6d8050c84083e4f7c861189`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138ea4c8ade2ab710ebb4bf11c9a449e034a7623fc36ec4bf53cd7b4684cf96`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782343db207d529a26e6e14f1fe6094ba3881b7f186aa414619c6b0bd66a1a0d`  
		Last Modified: Tue, 18 Mar 2025 18:00:57 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c807da6e0bc19d88df1dcffa2ff2eb50eafca7dceb2b0c24a05d2e47f3792`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b099078ed89a269a48bb93f33b013c288941cf91ef7a9820fc61f2dccc973f5`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:737cf84ed7a67e9cbdcd7f70938e322e7cbbfb25319bca652b06940f188c2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ad73c0f54384a2fa3d6fb5a46a9eb39b0b72913cba768969303ee5f7b93452`

```dockerfile
```

-	Layers:
	-	`sha256:4e103ade0760fb22db55fb6f3af4aa1562af7fc301a00a074ed879630b63525f`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:05883987356d7f2b28e785e0c98411791033e75c7594688eb66d1a0db75a892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130382942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc322d32470857db2fae3bcdcd6f94fa963581539b2bb5205ccd14009f56f816`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04248460f4f43dda114cf6e38bd72647f90344cc42043161295d8a77bb78f15a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 6.4 MB (6366336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248db7df30a00f0d2a17263b4f5d6b39ac19a2f086f95f1f7ee5181fbd6ff1a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7413c171635e268ad441559ac341509383d0976e68d8a2e9db87346c6d946e2`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2143b75dc215725319c90f47ba313cdbf7f5122e30ddb6f234dd5b6a770d`  
		Last Modified: Fri, 14 Mar 2025 21:11:59 GMT  
		Size: 55.6 MB (55593647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266db4b4f66e90d74f43dd7ded419a89c5a9e048191be6e81055e0e03d3f3a5a`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8cc5b9a67b353b2df6581e3a544618582ca576f2d7c79d45b87fb4ba98477`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:4a44e37e075a395cc4355a8aa3064dab865c450125c889f99cb5a8f470bf5bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d583b2c788713970578b9a323504d5586eec6c267e185a0b04bda8960c932fcb`

```dockerfile
```

-	Layers:
	-	`sha256:7e5ffd9071082203139db743e85aa7abfe2b617598eac876a4750cd6c30d3d8e`  
		Last Modified: Fri, 14 Mar 2025 21:11:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18846793853859ff87551bfc02c1ab4fb4bde786d6d46b87560be2e79e44c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132776864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c214e95d979948c88a170436f1ccac8784a86409f26db755cf9d2f70e8855d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820b82ff2c20ecc51faaa7954e0192ce1942c3e6bfd6c173d46cad0bcc80149`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 7.0 MB (6978857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9890e98c90e9be8547535746a1ce2ac835b9625992bb48bda3a6e519e59d941c`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0e0fb9ff9ad6077e9d11b776646112fff92c378d559ec25f96dcf382ec7516`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a8d5e617c46c4d436d58a462243b20e345b0b8dd62e6779a4dc38aaf3e995`  
		Last Modified: Wed, 19 Mar 2025 03:00:55 GMT  
		Size: 55.6 MB (55566422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ea02a3cc4e3e276ac3b3d2b23dc7379c994e36bb72c3503b009dd59a1fbe`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813784e7a533f0caa2d0e0215db30009c1516ebd5e23cc60655e83bd8b598260`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:254eb39d6d9f390c0125b2ca271f80deb85fe0c535d6ef6fb7f1672319809a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e9357138bca17b2f423400bdaffc1e096dcd4778dc7cfd21592e5a5b7f339`

```dockerfile
```

-	Layers:
	-	`sha256:d8091161332ca59b3d16e344df59f9a3dae230a3ea1d0703d8c69e415a02c8d8`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:b0cc8f27d36a03d30570d69d76615b84e4040bb52fd9c819bcb5a9cf1808d45d
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
$ docker pull docker@sha256:043c259759666d273afa94a9c9175a87a11f16cde2f613f4c527e4395b703a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74401810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbbfa15156e45896ae0baa0291763d59cbe8e9197af9396b1ce4d1c3fa92030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:054d1a0f0d9a7354f4ebcd12afbbe2a9020155beaa0ec46770c789ccbf1c7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e93df1fe28f45f774c9bf9ae35f4ca1912f62366ff899cafd275a526941419`

```dockerfile
```

-	Layers:
	-	`sha256:bac4c3a563812a6f84462124d368a71f165d3ee1ef9df06d3da71b7cca36e7d9`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:2af701b2acf52ac01aabe3f7b24129785436531e6994b6d19a75101c844b2aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69324552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f31a9e113936d6381be6fa03f180d10952d7db5923ef4da1db2e5c4d6ffb1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5e3d207e61cde6b1bc54354f37f0fbad8172bfc2584f0f5b511d0c598048f59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d14fb837116a45283ffadd7317ab0232cd066d977df7dc75bbd371ef47aed6`

```dockerfile
```

-	Layers:
	-	`sha256:0f25bf12b560e48dc887224d3f73240586d2726286656f557d257939d0aacae9`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:864e73fbbf97b3b2a57c6e72d332b7837b6ded3a278d4afa9e6777ebb5cdd5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68330712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00ed249c6b9ebcf5f398e457732ab11d2d31d789efee2927f9a5768620aa4b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 14 Mar 2025 11:04:27 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_VERSION=28.0.1
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Mar 2025 11:04:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Mar 2025 11:04:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2771de0165116b84662621b6ab21c653fd5a0e831c19632d56c2ad6511494d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7851d828c5af33e7f3518d627ee1eacf702912106be4bc93686f5213d4df2c3`

```dockerfile
```

-	Layers:
	-	`sha256:d7499afa1d7e720c1256ad1d97d24ebfce4a0b527055d56306c4ee3390c73d24`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9c69cedb70e576809b1c4bb33946ad8d85529f61c03e4b8f4641ef2e2c12c13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70126294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71220c9f3c0d88be6dd15374a7cde12582c3decef4a2ad6ac4ee45b346fd333f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a846f337948335ee9c66b55db9f4242f141b62ed0ac940a7308b6234a44672f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a466e3dd4f8d4aacc72abf776fe2dfb6d6eb6906cb0c1dd8bcca331951704947`

```dockerfile
```

-	Layers:
	-	`sha256:337cad1d65245942e78863cb17cababc17db3c09293347e6e4ce59e58b6d2e1c`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:828290aa6d563454a849d59ca1bdfb14804679fa96ac0ba8eeabd76ee73c145d
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
$ docker pull docker@sha256:6f284d567aabce6fc59489d515b32e9e9e3c434d56a30a5bb4c78e31f8ce4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141423867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ebdb25d1582b57307f7586f07df28009b8bfe0ccafff9ccf38d2ece7e6142d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b14dff50fdd36d583da1a62ad48743534c80d36636deb306ef3ea726fcc631b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c0320c0a080ec3869c570d9dcd47939db272e83fe901841e581fddfb923ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff3751a52465c2f4ca6f364704b34afeadb9a193f007f86b91faabe58e430298`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:66ed15e7c3455a7bd74e92449060237f9e6cd0c4a930a26cd8a90d344b555c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132050936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3635197fd3d2349cbe43887a8904a6cedcff1a4671bba7cab1a281c3bdaa98b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a710f976bef50357a64879fea6e83351c1d0ef59c4b2e03ab5c02c7d00693a`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 7.0 MB (7036932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd6d7147ebc3737f9054c3a2e0840f16cffd6eeb6d8050c84083e4f7c861189`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138ea4c8ade2ab710ebb4bf11c9a449e034a7623fc36ec4bf53cd7b4684cf96`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782343db207d529a26e6e14f1fe6094ba3881b7f186aa414619c6b0bd66a1a0d`  
		Last Modified: Tue, 18 Mar 2025 18:00:57 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c807da6e0bc19d88df1dcffa2ff2eb50eafca7dceb2b0c24a05d2e47f3792`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b099078ed89a269a48bb93f33b013c288941cf91ef7a9820fc61f2dccc973f5`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:737cf84ed7a67e9cbdcd7f70938e322e7cbbfb25319bca652b06940f188c2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ad73c0f54384a2fa3d6fb5a46a9eb39b0b72913cba768969303ee5f7b93452`

```dockerfile
```

-	Layers:
	-	`sha256:4e103ade0760fb22db55fb6f3af4aa1562af7fc301a00a074ed879630b63525f`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:05883987356d7f2b28e785e0c98411791033e75c7594688eb66d1a0db75a892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130382942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc322d32470857db2fae3bcdcd6f94fa963581539b2bb5205ccd14009f56f816`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04248460f4f43dda114cf6e38bd72647f90344cc42043161295d8a77bb78f15a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 6.4 MB (6366336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248db7df30a00f0d2a17263b4f5d6b39ac19a2f086f95f1f7ee5181fbd6ff1a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7413c171635e268ad441559ac341509383d0976e68d8a2e9db87346c6d946e2`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2143b75dc215725319c90f47ba313cdbf7f5122e30ddb6f234dd5b6a770d`  
		Last Modified: Fri, 14 Mar 2025 21:11:59 GMT  
		Size: 55.6 MB (55593647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266db4b4f66e90d74f43dd7ded419a89c5a9e048191be6e81055e0e03d3f3a5a`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8cc5b9a67b353b2df6581e3a544618582ca576f2d7c79d45b87fb4ba98477`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4a44e37e075a395cc4355a8aa3064dab865c450125c889f99cb5a8f470bf5bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d583b2c788713970578b9a323504d5586eec6c267e185a0b04bda8960c932fcb`

```dockerfile
```

-	Layers:
	-	`sha256:7e5ffd9071082203139db743e85aa7abfe2b617598eac876a4750cd6c30d3d8e`  
		Last Modified: Fri, 14 Mar 2025 21:11:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18846793853859ff87551bfc02c1ab4fb4bde786d6d46b87560be2e79e44c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132776864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c214e95d979948c88a170436f1ccac8784a86409f26db755cf9d2f70e8855d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820b82ff2c20ecc51faaa7954e0192ce1942c3e6bfd6c173d46cad0bcc80149`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 7.0 MB (6978857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9890e98c90e9be8547535746a1ce2ac835b9625992bb48bda3a6e519e59d941c`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0e0fb9ff9ad6077e9d11b776646112fff92c378d559ec25f96dcf382ec7516`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a8d5e617c46c4d436d58a462243b20e345b0b8dd62e6779a4dc38aaf3e995`  
		Last Modified: Wed, 19 Mar 2025 03:00:55 GMT  
		Size: 55.6 MB (55566422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ea02a3cc4e3e276ac3b3d2b23dc7379c994e36bb72c3503b009dd59a1fbe`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813784e7a533f0caa2d0e0215db30009c1516ebd5e23cc60655e83bd8b598260`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:254eb39d6d9f390c0125b2ca271f80deb85fe0c535d6ef6fb7f1672319809a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e9357138bca17b2f423400bdaffc1e096dcd4778dc7cfd21592e5a5b7f339`

```dockerfile
```

-	Layers:
	-	`sha256:d8091161332ca59b3d16e344df59f9a3dae230a3ea1d0703d8c69e415a02c8d8`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:754aa7c1bfd9b5dad719015ad9357a0c7a66f3bde2c932b22ff1684357563eb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:32dfa25aad31337bd5141ba8380e0288c5aba973e0d1013d30cdd080ee500eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159578202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66f208fb1c578feb5ab1bbafb38911d9d47973065e3e2a8d5f7448be4c121c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8142c21eb3ac89c3e91203a0f16eb4cd39edb96ed809c12850cc330d6cdbea30`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 986.6 KB (986583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3424f6c492d784bb37beb7ab00c8b859ce13297717dc058ad18fe672c9ff69`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711170e2dc3314d2bc5e383d4df9bfeb3a49f7f56568960e8641335a124cc79`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d519ed6a081ab4200ce5e80dbea1046b066972f89c82dfe38ec962f51b7bec00`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 17.2 MB (17166411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd10a25c4410d07e25fcf12f7f25f5c8cb517a5b7be041a8c49574903667d34`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bcfeee32b0e1597300ac937a9a375e876a3ebf5644f4cfc31af89aa04e6cf1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843ea3c71e7950d1793b6c27c89054c2752811c275ea6a0c88ec2f47ad44c264`

```dockerfile
```

-	Layers:
	-	`sha256:0434e0329e64168242a488dc2ec087d57bbe6f29f380339d8b4c8a3e79e5bce6`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:19e4800a186f237d40cbcef2b6703bef220e7bc5c52f0df68845b5a65e50dbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153065629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e0d8637a09a7e5fc0e156a815f870279820b8f7c6bd846366df78e37aab5c7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de7b18622f97a3c1064dce569f3ff7a45ce5eefdf7e45c63fbe82ad6369360d`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 8.1 MB (8076411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e796aa6b98c5b6ef094554192c9676616631c209858d78a497ad8e57a085f1dc`  
		Last Modified: Fri, 14 Mar 2025 21:49:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cac35bcba55fd0892cfa0fd723ea433271f4a7bce0a06e6817a2278acd9aad7`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 18.4 MB (18425653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46c4ca48b2cb3e83a2c78785255753f121b7d03854e34c6d7c787ce45d8b60`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 20.0 MB (20040986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11e199ee8eacbea69e12a4fb23b40f68ea0b4f1ab759f2131291d19402cb3b`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 19.6 MB (19581878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dce91693c540282e494983ba2524586f9cd6b97f769eb795b4d852e7fdd581`  
		Last Modified: Fri, 14 Mar 2025 21:49:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438358ebfbee95af11c2bfbf1b71df6e9c81aace1fc12187b64c58aaf900d77e`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df88cc4d1057f2f914bc664a4b82a142b8dcf06a77e87a9516eae14364f033a4`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35dcd7757e18c2324a8fc638d2a9ea3e74daad9f8cc5877a2eaa68b7942c60`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 7.0 MB (6978811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69aeae86dcdffdf63366bcf9bbb61336fe9a67fcecbe8d29aa8b83b292002c`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 99.4 KB (99380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e216e0fa6851d219c9c6c2188ef5eab27b52103511d70e675d082ca22096e8`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2947322861bdc5f37e9119d204f26fd249623e0295d104af44bd1673c09a1663`  
		Last Modified: Fri, 14 Mar 2025 23:43:12 GMT  
		Size: 55.6 MB (55566453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170de84416a27698febebda6b66c8758b52aaa68d72775b3d83ca68f5561627f`  
		Last Modified: Fri, 14 Mar 2025 23:43:11 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa622cc428daff0de20c56abfa4b13ed8ea8323c3f1a30cd9c0f36b258be4aae`  
		Last Modified: Fri, 14 Mar 2025 23:43:11 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87d24bb402bee44662ae05f56a7f802abb4bfe4946eed38e6b92e30346bec96`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 1.0 MB (1014190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c69a48222fb6f42109b9a380dbfa4be336a0a0c016cd37d8619fae6835b85f`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64568427128fb5786c46527a81ed74941db093f35e996be0cf0d4ccba9f08482`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0ec1b2a82774ea69637c04bae551f0d327110921726fb1157674fe476b5a2`  
		Last Modified: Sat, 15 Mar 2025 00:10:32 GMT  
		Size: 19.3 MB (19279437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9574ada033fbed6c291f9ef3bc394ce883d5895ae06ae89797ddc2f3641de2e9`  
		Last Modified: Sat, 15 Mar 2025 00:10:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4537a5f78b6c74f3425552daffd342a3df407e99b582f9a04cc4edbe634b8ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ea771efeb5e1e724113f140d2fa43a5020ffd247c91f8542a8d7e3af0f08db`

```dockerfile
```

-	Layers:
	-	`sha256:c66d401445d485c1954b2c479641d5a36e9cd483c0110f40cab705706d4f2f3c`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:80ada8b5544018710daaf3e0df8c13fc9467ca8dab197647f5fb2011e476d13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:81996f945dd6afd17a2f454f627cc9301a6d669d579eee88075c6866592b7eac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974045827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90411219e91a7a2282d6bafa1fa9f88374b9cc7fc5023a00346072afe20d252f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 18 Mar 2025 17:48:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:59 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:49:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:49:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:13 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:49:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:49:15 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:49:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:49:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:49:28 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:49:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0cd020c6471f62220ad8ed2ae2b3772b806f467cb0f11bc4308b9f2d0d26a`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cf4955d1aad1f83447efbdbcf08c9bd7423c84e7c6ac5bc6a5625140c991e0`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 400.2 KB (400166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90786f2c40deca413eed711fbbeb0abe197cababcf2e8b187fda5466bf3f9e14`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684238c758b95728bef5bbcf3815bce65fcb21040c3ec400e17b2e4b2975988`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7eac4b401484a405d9d595d4ab1ab2e2fa8f1dc11da64e453e0d575e376817`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 19.9 MB (19862606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68379e676f653db1ef6496f93f7f34f94e2e6adc3897f119f4d93a2092313f0`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df3c74807df3393363f62fd1b3dec83fe3a43f74559b92815cd5cbd580fbe6f`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5332d7c8bb3be4f3f08437752f48d8a66371aad10f5328510eeaa532db9383ba`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebe5ad6be9c69cb89a53b45d42605e0654403950049245df6ed82d6552beb2`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.8 MB (22789480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7945eb3de2b551bb141ecdcf88f5508c82ba67aa0f4910a08e9833a279946fde`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32749cc1ae150ad64cd11025c4de890ad6f72d84ccb8714200245b156bf136d1`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598bafa4dd3f7f04b9861f17341c80a693efdf2c84a11ab664533e4b3c2334b2`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b541b6491c1b4a89b6665a2775f4c706b4f2d8349747d04f83ac14f4ac23ca`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.3 MB (22334051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:83ff96ddbee1bd02aa91285b3bf9690d98b899aff79585b714f4db4fa5fffcc7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335201497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a81d38ebdc303a8a3364a74efe23a1bedf44c1d7b8e6eed9a8be08f2556ec27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 18 Mar 2025 17:48:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:18 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:48:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:48:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:28 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:48:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:48:30 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:48:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:48:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:48:41 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:48:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f078092de8abb6d57d53e680c3076c9ef2bfbbf71c6f4a21348b227be48e4`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf4f863fc1275088515214a01de99ac68d3bfe956ba35597d3baa916414bfc7`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 364.5 KB (364474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6be91d2a668f124038a4b58fd4ea66112de7b5b0b97a139693dfad7af569f`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2113532490862d3f6fbbc444054df6a45ac27fd7df836514bba886616282d1e`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed759800fa7e1df988ee6bd77b70fb0ff86c479116b939808e48316290b16876`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 19.8 MB (19826177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8359603b2119f0fa8a6571abae59b6fedadab69d593491f5654da2369da6101`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8691616fbb1ac24ed70ed40459202a0890dc879db4b4bd145bf682fe91a5f35d`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fede937bf0332135d9e85cd74b71cdabff018cd49fdb00377c1c8b6a955a98`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df182fa0d8efc357ce076453fa75808da26e64d896888a663012d878865f2516`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.8 MB (22756719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662cc6465c91f282c1f13da905ddbb3283da516701570a3ba3bbee34f45732ee`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ce90bd08504a907b943a9371e9bc6cee33b2bfce11817ab311fde6581cf9a6`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afc5eb0fd1f12683a0f679fa6e3e6ec671d4c5216693af8d75aae719eb8775f`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab8c7824ed6e25645587020a647c04eb9024db067d572ea1afed4d07eb063a`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.3 MB (22301399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:8b2723933f4e20b03d82fad4f272979c45d21e29d5d5437a257dddd7a19b69e9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216826173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad7864511de6cf197875bc99d7c27cee1e5e4a9511cdb529bf075ad6e87eed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 18 Mar 2025 17:52:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:53:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:53:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:53:59 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:54:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:54:10 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:54:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efae6d46cdd88fc96e587336604ae353dae631d3edfb17299749b56f042f86e`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabff009c2b284cea2d40695c1b44d8b2e2b9a499dca58e92884fc4c4139d19b`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 338.8 KB (338767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299a5346171e96e11bbf7e75d2c923c9e767db919ae268e6303f0a8b51505132`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5681385a5fb68fbaf1d531ba43ef1a4eebca86ff9357c638c2b7ab8722096c`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bf621533bae634d522d1baa809d4030a69957056c545455ed8a6b54a582f37`  
		Last Modified: Tue, 18 Mar 2025 17:54:28 GMT  
		Size: 19.8 MB (19814343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d74b41781047bb821590370c205f708cb1312ac611cf3ffa7d92817cb3385`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8fd088b8dce22bb00a6dae4b3c11ff824bc93bbd5375cf39d193367b61b418`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c212d22018c8ed56b082699241fba4b6a975dcc80941663d3333e79726ef710`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120f89b8213b7712056cc20c3454b43dfbefee8092827722ba2bd7183f6693ea`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.7 MB (22744744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbe59c92ae308cc1ca95460830da582ea729bd502e6fdcc9e91a0980a0cf7f0`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24199190c27c55807d7aa76cacb9f25e09fbcbaf0385f92d8088eed73e875917`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f962b02a3d44056e12be508848bc41eb716d98ca72374c1e979fbcd1cf7c7`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ac0a28f0cff7f101228c34c93dbaf640a640f1ee5472053393f4931082d129`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.3 MB (22281907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:c780cf7ac1c5c0cb9599b2df0349dc29186be36aae111d30e399c208f227ae72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:8b2723933f4e20b03d82fad4f272979c45d21e29d5d5437a257dddd7a19b69e9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216826173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad7864511de6cf197875bc99d7c27cee1e5e4a9511cdb529bf075ad6e87eed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 18 Mar 2025 17:52:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:53:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:53:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:53:59 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:54:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:54:10 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:54:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efae6d46cdd88fc96e587336604ae353dae631d3edfb17299749b56f042f86e`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabff009c2b284cea2d40695c1b44d8b2e2b9a499dca58e92884fc4c4139d19b`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 338.8 KB (338767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299a5346171e96e11bbf7e75d2c923c9e767db919ae268e6303f0a8b51505132`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5681385a5fb68fbaf1d531ba43ef1a4eebca86ff9357c638c2b7ab8722096c`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bf621533bae634d522d1baa809d4030a69957056c545455ed8a6b54a582f37`  
		Last Modified: Tue, 18 Mar 2025 17:54:28 GMT  
		Size: 19.8 MB (19814343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d74b41781047bb821590370c205f708cb1312ac611cf3ffa7d92817cb3385`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8fd088b8dce22bb00a6dae4b3c11ff824bc93bbd5375cf39d193367b61b418`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c212d22018c8ed56b082699241fba4b6a975dcc80941663d3333e79726ef710`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120f89b8213b7712056cc20c3454b43dfbefee8092827722ba2bd7183f6693ea`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.7 MB (22744744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbe59c92ae308cc1ca95460830da582ea729bd502e6fdcc9e91a0980a0cf7f0`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24199190c27c55807d7aa76cacb9f25e09fbcbaf0385f92d8088eed73e875917`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f962b02a3d44056e12be508848bc41eb716d98ca72374c1e979fbcd1cf7c7`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ac0a28f0cff7f101228c34c93dbaf640a640f1ee5472053393f4931082d129`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.3 MB (22281907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:1602a0714e35d9428df55b3574afa737262d7899f2981edad083d6958065b422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:83ff96ddbee1bd02aa91285b3bf9690d98b899aff79585b714f4db4fa5fffcc7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335201497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a81d38ebdc303a8a3364a74efe23a1bedf44c1d7b8e6eed9a8be08f2556ec27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 18 Mar 2025 17:48:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:18 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:48:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:48:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:28 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:48:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:48:30 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:48:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:48:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:48:41 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:48:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f078092de8abb6d57d53e680c3076c9ef2bfbbf71c6f4a21348b227be48e4`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf4f863fc1275088515214a01de99ac68d3bfe956ba35597d3baa916414bfc7`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 364.5 KB (364474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6be91d2a668f124038a4b58fd4ea66112de7b5b0b97a139693dfad7af569f`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2113532490862d3f6fbbc444054df6a45ac27fd7df836514bba886616282d1e`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed759800fa7e1df988ee6bd77b70fb0ff86c479116b939808e48316290b16876`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 19.8 MB (19826177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8359603b2119f0fa8a6571abae59b6fedadab69d593491f5654da2369da6101`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8691616fbb1ac24ed70ed40459202a0890dc879db4b4bd145bf682fe91a5f35d`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fede937bf0332135d9e85cd74b71cdabff018cd49fdb00377c1c8b6a955a98`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df182fa0d8efc357ce076453fa75808da26e64d896888a663012d878865f2516`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.8 MB (22756719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662cc6465c91f282c1f13da905ddbb3283da516701570a3ba3bbee34f45732ee`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ce90bd08504a907b943a9371e9bc6cee33b2bfce11817ab311fde6581cf9a6`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afc5eb0fd1f12683a0f679fa6e3e6ec671d4c5216693af8d75aae719eb8775f`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab8c7824ed6e25645587020a647c04eb9024db067d572ea1afed4d07eb063a`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.3 MB (22301399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:4c2d528f844dac99062dc79967dd48348177d2db9ea7c66e86dd29010b571301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:81996f945dd6afd17a2f454f627cc9301a6d669d579eee88075c6866592b7eac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974045827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90411219e91a7a2282d6bafa1fa9f88374b9cc7fc5023a00346072afe20d252f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 18 Mar 2025 17:48:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:59 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:49:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:49:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:13 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:49:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:49:15 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:49:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:49:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:49:28 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:49:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0cd020c6471f62220ad8ed2ae2b3772b806f467cb0f11bc4308b9f2d0d26a`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cf4955d1aad1f83447efbdbcf08c9bd7423c84e7c6ac5bc6a5625140c991e0`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 400.2 KB (400166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90786f2c40deca413eed711fbbeb0abe197cababcf2e8b187fda5466bf3f9e14`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684238c758b95728bef5bbcf3815bce65fcb21040c3ec400e17b2e4b2975988`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7eac4b401484a405d9d595d4ab1ab2e2fa8f1dc11da64e453e0d575e376817`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 19.9 MB (19862606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68379e676f653db1ef6496f93f7f34f94e2e6adc3897f119f4d93a2092313f0`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df3c74807df3393363f62fd1b3dec83fe3a43f74559b92815cd5cbd580fbe6f`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5332d7c8bb3be4f3f08437752f48d8a66371aad10f5328510eeaa532db9383ba`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebe5ad6be9c69cb89a53b45d42605e0654403950049245df6ed82d6552beb2`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.8 MB (22789480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7945eb3de2b551bb141ecdcf88f5508c82ba67aa0f4910a08e9833a279946fde`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32749cc1ae150ad64cd11025c4de890ad6f72d84ccb8714200245b156bf136d1`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598bafa4dd3f7f04b9861f17341c80a693efdf2c84a11ab664533e4b3c2334b2`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b541b6491c1b4a89b6665a2775f4c706b4f2d8349747d04f83ac14f4ac23ca`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.3 MB (22334051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0`

```console
$ docker pull docker@sha256:828290aa6d563454a849d59ca1bdfb14804679fa96ac0ba8eeabd76ee73c145d
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

### `docker:28.0` - linux; amd64

```console
$ docker pull docker@sha256:6f284d567aabce6fc59489d515b32e9e9e3c434d56a30a5bb4c78e31f8ce4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141423867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ebdb25d1582b57307f7586f07df28009b8bfe0ccafff9ccf38d2ece7e6142d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:b14dff50fdd36d583da1a62ad48743534c80d36636deb306ef3ea726fcc631b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c0320c0a080ec3869c570d9dcd47939db272e83fe901841e581fddfb923ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff3751a52465c2f4ca6f364704b34afeadb9a193f007f86b91faabe58e430298`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:66ed15e7c3455a7bd74e92449060237f9e6cd0c4a930a26cd8a90d344b555c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132050936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3635197fd3d2349cbe43887a8904a6cedcff1a4671bba7cab1a281c3bdaa98b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a710f976bef50357a64879fea6e83351c1d0ef59c4b2e03ab5c02c7d00693a`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 7.0 MB (7036932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd6d7147ebc3737f9054c3a2e0840f16cffd6eeb6d8050c84083e4f7c861189`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138ea4c8ade2ab710ebb4bf11c9a449e034a7623fc36ec4bf53cd7b4684cf96`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782343db207d529a26e6e14f1fe6094ba3881b7f186aa414619c6b0bd66a1a0d`  
		Last Modified: Tue, 18 Mar 2025 18:00:57 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c807da6e0bc19d88df1dcffa2ff2eb50eafca7dceb2b0c24a05d2e47f3792`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b099078ed89a269a48bb93f33b013c288941cf91ef7a9820fc61f2dccc973f5`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:737cf84ed7a67e9cbdcd7f70938e322e7cbbfb25319bca652b06940f188c2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ad73c0f54384a2fa3d6fb5a46a9eb39b0b72913cba768969303ee5f7b93452`

```dockerfile
```

-	Layers:
	-	`sha256:4e103ade0760fb22db55fb6f3af4aa1562af7fc301a00a074ed879630b63525f`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:05883987356d7f2b28e785e0c98411791033e75c7594688eb66d1a0db75a892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130382942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc322d32470857db2fae3bcdcd6f94fa963581539b2bb5205ccd14009f56f816`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04248460f4f43dda114cf6e38bd72647f90344cc42043161295d8a77bb78f15a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 6.4 MB (6366336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248db7df30a00f0d2a17263b4f5d6b39ac19a2f086f95f1f7ee5181fbd6ff1a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7413c171635e268ad441559ac341509383d0976e68d8a2e9db87346c6d946e2`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2143b75dc215725319c90f47ba313cdbf7f5122e30ddb6f234dd5b6a770d`  
		Last Modified: Fri, 14 Mar 2025 21:11:59 GMT  
		Size: 55.6 MB (55593647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266db4b4f66e90d74f43dd7ded419a89c5a9e048191be6e81055e0e03d3f3a5a`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8cc5b9a67b353b2df6581e3a544618582ca576f2d7c79d45b87fb4ba98477`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:4a44e37e075a395cc4355a8aa3064dab865c450125c889f99cb5a8f470bf5bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d583b2c788713970578b9a323504d5586eec6c267e185a0b04bda8960c932fcb`

```dockerfile
```

-	Layers:
	-	`sha256:7e5ffd9071082203139db743e85aa7abfe2b617598eac876a4750cd6c30d3d8e`  
		Last Modified: Fri, 14 Mar 2025 21:11:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18846793853859ff87551bfc02c1ab4fb4bde786d6d46b87560be2e79e44c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132776864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c214e95d979948c88a170436f1ccac8784a86409f26db755cf9d2f70e8855d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820b82ff2c20ecc51faaa7954e0192ce1942c3e6bfd6c173d46cad0bcc80149`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 7.0 MB (6978857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9890e98c90e9be8547535746a1ce2ac835b9625992bb48bda3a6e519e59d941c`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0e0fb9ff9ad6077e9d11b776646112fff92c378d559ec25f96dcf382ec7516`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a8d5e617c46c4d436d58a462243b20e345b0b8dd62e6779a4dc38aaf3e995`  
		Last Modified: Wed, 19 Mar 2025 03:00:55 GMT  
		Size: 55.6 MB (55566422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ea02a3cc4e3e276ac3b3d2b23dc7379c994e36bb72c3503b009dd59a1fbe`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813784e7a533f0caa2d0e0215db30009c1516ebd5e23cc60655e83bd8b598260`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:254eb39d6d9f390c0125b2ca271f80deb85fe0c535d6ef6fb7f1672319809a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e9357138bca17b2f423400bdaffc1e096dcd4778dc7cfd21592e5a5b7f339`

```dockerfile
```

-	Layers:
	-	`sha256:d8091161332ca59b3d16e344df59f9a3dae230a3ea1d0703d8c69e415a02c8d8`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-cli`

```console
$ docker pull docker@sha256:b0cc8f27d36a03d30570d69d76615b84e4040bb52fd9c819bcb5a9cf1808d45d
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

### `docker:28.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:043c259759666d273afa94a9c9175a87a11f16cde2f613f4c527e4395b703a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74401810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbbfa15156e45896ae0baa0291763d59cbe8e9197af9396b1ce4d1c3fa92030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:054d1a0f0d9a7354f4ebcd12afbbe2a9020155beaa0ec46770c789ccbf1c7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e93df1fe28f45f774c9bf9ae35f4ca1912f62366ff899cafd275a526941419`

```dockerfile
```

-	Layers:
	-	`sha256:bac4c3a563812a6f84462124d368a71f165d3ee1ef9df06d3da71b7cca36e7d9`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:2af701b2acf52ac01aabe3f7b24129785436531e6994b6d19a75101c844b2aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69324552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f31a9e113936d6381be6fa03f180d10952d7db5923ef4da1db2e5c4d6ffb1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5e3d207e61cde6b1bc54354f37f0fbad8172bfc2584f0f5b511d0c598048f59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d14fb837116a45283ffadd7317ab0232cd066d977df7dc75bbd371ef47aed6`

```dockerfile
```

-	Layers:
	-	`sha256:0f25bf12b560e48dc887224d3f73240586d2726286656f557d257939d0aacae9`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:864e73fbbf97b3b2a57c6e72d332b7837b6ded3a278d4afa9e6777ebb5cdd5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68330712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00ed249c6b9ebcf5f398e457732ab11d2d31d789efee2927f9a5768620aa4b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 14 Mar 2025 11:04:27 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_VERSION=28.0.1
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Mar 2025 11:04:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Mar 2025 11:04:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2771de0165116b84662621b6ab21c653fd5a0e831c19632d56c2ad6511494d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7851d828c5af33e7f3518d627ee1eacf702912106be4bc93686f5213d4df2c3`

```dockerfile
```

-	Layers:
	-	`sha256:d7499afa1d7e720c1256ad1d97d24ebfce4a0b527055d56306c4ee3390c73d24`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9c69cedb70e576809b1c4bb33946ad8d85529f61c03e4b8f4641ef2e2c12c13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70126294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71220c9f3c0d88be6dd15374a7cde12582c3decef4a2ad6ac4ee45b346fd333f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a846f337948335ee9c66b55db9f4242f141b62ed0ac940a7308b6234a44672f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a466e3dd4f8d4aacc72abf776fe2dfb6d6eb6906cb0c1dd8bcca331951704947`

```dockerfile
```

-	Layers:
	-	`sha256:337cad1d65245942e78863cb17cababc17db3c09293347e6e4ce59e58b6d2e1c`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-dind`

```console
$ docker pull docker@sha256:828290aa6d563454a849d59ca1bdfb14804679fa96ac0ba8eeabd76ee73c145d
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

### `docker:28.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:6f284d567aabce6fc59489d515b32e9e9e3c434d56a30a5bb4c78e31f8ce4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141423867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ebdb25d1582b57307f7586f07df28009b8bfe0ccafff9ccf38d2ece7e6142d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b14dff50fdd36d583da1a62ad48743534c80d36636deb306ef3ea726fcc631b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c0320c0a080ec3869c570d9dcd47939db272e83fe901841e581fddfb923ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff3751a52465c2f4ca6f364704b34afeadb9a193f007f86b91faabe58e430298`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:66ed15e7c3455a7bd74e92449060237f9e6cd0c4a930a26cd8a90d344b555c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132050936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3635197fd3d2349cbe43887a8904a6cedcff1a4671bba7cab1a281c3bdaa98b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a710f976bef50357a64879fea6e83351c1d0ef59c4b2e03ab5c02c7d00693a`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 7.0 MB (7036932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd6d7147ebc3737f9054c3a2e0840f16cffd6eeb6d8050c84083e4f7c861189`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138ea4c8ade2ab710ebb4bf11c9a449e034a7623fc36ec4bf53cd7b4684cf96`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782343db207d529a26e6e14f1fe6094ba3881b7f186aa414619c6b0bd66a1a0d`  
		Last Modified: Tue, 18 Mar 2025 18:00:57 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c807da6e0bc19d88df1dcffa2ff2eb50eafca7dceb2b0c24a05d2e47f3792`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b099078ed89a269a48bb93f33b013c288941cf91ef7a9820fc61f2dccc973f5`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:737cf84ed7a67e9cbdcd7f70938e322e7cbbfb25319bca652b06940f188c2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ad73c0f54384a2fa3d6fb5a46a9eb39b0b72913cba768969303ee5f7b93452`

```dockerfile
```

-	Layers:
	-	`sha256:4e103ade0760fb22db55fb6f3af4aa1562af7fc301a00a074ed879630b63525f`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:05883987356d7f2b28e785e0c98411791033e75c7594688eb66d1a0db75a892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130382942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc322d32470857db2fae3bcdcd6f94fa963581539b2bb5205ccd14009f56f816`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04248460f4f43dda114cf6e38bd72647f90344cc42043161295d8a77bb78f15a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 6.4 MB (6366336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248db7df30a00f0d2a17263b4f5d6b39ac19a2f086f95f1f7ee5181fbd6ff1a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7413c171635e268ad441559ac341509383d0976e68d8a2e9db87346c6d946e2`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2143b75dc215725319c90f47ba313cdbf7f5122e30ddb6f234dd5b6a770d`  
		Last Modified: Fri, 14 Mar 2025 21:11:59 GMT  
		Size: 55.6 MB (55593647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266db4b4f66e90d74f43dd7ded419a89c5a9e048191be6e81055e0e03d3f3a5a`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8cc5b9a67b353b2df6581e3a544618582ca576f2d7c79d45b87fb4ba98477`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4a44e37e075a395cc4355a8aa3064dab865c450125c889f99cb5a8f470bf5bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d583b2c788713970578b9a323504d5586eec6c267e185a0b04bda8960c932fcb`

```dockerfile
```

-	Layers:
	-	`sha256:7e5ffd9071082203139db743e85aa7abfe2b617598eac876a4750cd6c30d3d8e`  
		Last Modified: Fri, 14 Mar 2025 21:11:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18846793853859ff87551bfc02c1ab4fb4bde786d6d46b87560be2e79e44c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132776864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c214e95d979948c88a170436f1ccac8784a86409f26db755cf9d2f70e8855d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820b82ff2c20ecc51faaa7954e0192ce1942c3e6bfd6c173d46cad0bcc80149`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 7.0 MB (6978857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9890e98c90e9be8547535746a1ce2ac835b9625992bb48bda3a6e519e59d941c`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0e0fb9ff9ad6077e9d11b776646112fff92c378d559ec25f96dcf382ec7516`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a8d5e617c46c4d436d58a462243b20e345b0b8dd62e6779a4dc38aaf3e995`  
		Last Modified: Wed, 19 Mar 2025 03:00:55 GMT  
		Size: 55.6 MB (55566422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ea02a3cc4e3e276ac3b3d2b23dc7379c994e36bb72c3503b009dd59a1fbe`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813784e7a533f0caa2d0e0215db30009c1516ebd5e23cc60655e83bd8b598260`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:254eb39d6d9f390c0125b2ca271f80deb85fe0c535d6ef6fb7f1672319809a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e9357138bca17b2f423400bdaffc1e096dcd4778dc7cfd21592e5a5b7f339`

```dockerfile
```

-	Layers:
	-	`sha256:d8091161332ca59b3d16e344df59f9a3dae230a3ea1d0703d8c69e415a02c8d8`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-dind-rootless`

```console
$ docker pull docker@sha256:754aa7c1bfd9b5dad719015ad9357a0c7a66f3bde2c932b22ff1684357563eb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:32dfa25aad31337bd5141ba8380e0288c5aba973e0d1013d30cdd080ee500eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159578202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66f208fb1c578feb5ab1bbafb38911d9d47973065e3e2a8d5f7448be4c121c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8142c21eb3ac89c3e91203a0f16eb4cd39edb96ed809c12850cc330d6cdbea30`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 986.6 KB (986583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3424f6c492d784bb37beb7ab00c8b859ce13297717dc058ad18fe672c9ff69`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711170e2dc3314d2bc5e383d4df9bfeb3a49f7f56568960e8641335a124cc79`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d519ed6a081ab4200ce5e80dbea1046b066972f89c82dfe38ec962f51b7bec00`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 17.2 MB (17166411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd10a25c4410d07e25fcf12f7f25f5c8cb517a5b7be041a8c49574903667d34`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bcfeee32b0e1597300ac937a9a375e876a3ebf5644f4cfc31af89aa04e6cf1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843ea3c71e7950d1793b6c27c89054c2752811c275ea6a0c88ec2f47ad44c264`

```dockerfile
```

-	Layers:
	-	`sha256:0434e0329e64168242a488dc2ec087d57bbe6f29f380339d8b4c8a3e79e5bce6`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:19e4800a186f237d40cbcef2b6703bef220e7bc5c52f0df68845b5a65e50dbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153065629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e0d8637a09a7e5fc0e156a815f870279820b8f7c6bd846366df78e37aab5c7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de7b18622f97a3c1064dce569f3ff7a45ce5eefdf7e45c63fbe82ad6369360d`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 8.1 MB (8076411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e796aa6b98c5b6ef094554192c9676616631c209858d78a497ad8e57a085f1dc`  
		Last Modified: Fri, 14 Mar 2025 21:49:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cac35bcba55fd0892cfa0fd723ea433271f4a7bce0a06e6817a2278acd9aad7`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 18.4 MB (18425653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46c4ca48b2cb3e83a2c78785255753f121b7d03854e34c6d7c787ce45d8b60`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 20.0 MB (20040986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11e199ee8eacbea69e12a4fb23b40f68ea0b4f1ab759f2131291d19402cb3b`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 19.6 MB (19581878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dce91693c540282e494983ba2524586f9cd6b97f769eb795b4d852e7fdd581`  
		Last Modified: Fri, 14 Mar 2025 21:49:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438358ebfbee95af11c2bfbf1b71df6e9c81aace1fc12187b64c58aaf900d77e`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df88cc4d1057f2f914bc664a4b82a142b8dcf06a77e87a9516eae14364f033a4`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35dcd7757e18c2324a8fc638d2a9ea3e74daad9f8cc5877a2eaa68b7942c60`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 7.0 MB (6978811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69aeae86dcdffdf63366bcf9bbb61336fe9a67fcecbe8d29aa8b83b292002c`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 99.4 KB (99380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e216e0fa6851d219c9c6c2188ef5eab27b52103511d70e675d082ca22096e8`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2947322861bdc5f37e9119d204f26fd249623e0295d104af44bd1673c09a1663`  
		Last Modified: Fri, 14 Mar 2025 23:43:12 GMT  
		Size: 55.6 MB (55566453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170de84416a27698febebda6b66c8758b52aaa68d72775b3d83ca68f5561627f`  
		Last Modified: Fri, 14 Mar 2025 23:43:11 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa622cc428daff0de20c56abfa4b13ed8ea8323c3f1a30cd9c0f36b258be4aae`  
		Last Modified: Fri, 14 Mar 2025 23:43:11 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87d24bb402bee44662ae05f56a7f802abb4bfe4946eed38e6b92e30346bec96`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 1.0 MB (1014190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c69a48222fb6f42109b9a380dbfa4be336a0a0c016cd37d8619fae6835b85f`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64568427128fb5786c46527a81ed74941db093f35e996be0cf0d4ccba9f08482`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0ec1b2a82774ea69637c04bae551f0d327110921726fb1157674fe476b5a2`  
		Last Modified: Sat, 15 Mar 2025 00:10:32 GMT  
		Size: 19.3 MB (19279437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9574ada033fbed6c291f9ef3bc394ce883d5895ae06ae89797ddc2f3641de2e9`  
		Last Modified: Sat, 15 Mar 2025 00:10:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4537a5f78b6c74f3425552daffd342a3df407e99b582f9a04cc4edbe634b8ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ea771efeb5e1e724113f140d2fa43a5020ffd247c91f8542a8d7e3af0f08db`

```dockerfile
```

-	Layers:
	-	`sha256:c66d401445d485c1954b2c479641d5a36e9cd483c0110f40cab705706d4f2f3c`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-windowsservercore`

```console
$ docker pull docker@sha256:80ada8b5544018710daaf3e0df8c13fc9467ca8dab197647f5fb2011e476d13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:81996f945dd6afd17a2f454f627cc9301a6d669d579eee88075c6866592b7eac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974045827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90411219e91a7a2282d6bafa1fa9f88374b9cc7fc5023a00346072afe20d252f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 18 Mar 2025 17:48:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:59 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:49:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:49:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:13 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:49:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:49:15 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:49:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:49:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:49:28 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:49:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0cd020c6471f62220ad8ed2ae2b3772b806f467cb0f11bc4308b9f2d0d26a`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cf4955d1aad1f83447efbdbcf08c9bd7423c84e7c6ac5bc6a5625140c991e0`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 400.2 KB (400166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90786f2c40deca413eed711fbbeb0abe197cababcf2e8b187fda5466bf3f9e14`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684238c758b95728bef5bbcf3815bce65fcb21040c3ec400e17b2e4b2975988`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7eac4b401484a405d9d595d4ab1ab2e2fa8f1dc11da64e453e0d575e376817`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 19.9 MB (19862606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68379e676f653db1ef6496f93f7f34f94e2e6adc3897f119f4d93a2092313f0`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df3c74807df3393363f62fd1b3dec83fe3a43f74559b92815cd5cbd580fbe6f`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5332d7c8bb3be4f3f08437752f48d8a66371aad10f5328510eeaa532db9383ba`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebe5ad6be9c69cb89a53b45d42605e0654403950049245df6ed82d6552beb2`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.8 MB (22789480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7945eb3de2b551bb141ecdcf88f5508c82ba67aa0f4910a08e9833a279946fde`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32749cc1ae150ad64cd11025c4de890ad6f72d84ccb8714200245b156bf136d1`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598bafa4dd3f7f04b9861f17341c80a693efdf2c84a11ab664533e4b3c2334b2`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b541b6491c1b4a89b6665a2775f4c706b4f2d8349747d04f83ac14f4ac23ca`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.3 MB (22334051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:83ff96ddbee1bd02aa91285b3bf9690d98b899aff79585b714f4db4fa5fffcc7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335201497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a81d38ebdc303a8a3364a74efe23a1bedf44c1d7b8e6eed9a8be08f2556ec27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 18 Mar 2025 17:48:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:18 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:48:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:48:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:28 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:48:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:48:30 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:48:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:48:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:48:41 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:48:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f078092de8abb6d57d53e680c3076c9ef2bfbbf71c6f4a21348b227be48e4`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf4f863fc1275088515214a01de99ac68d3bfe956ba35597d3baa916414bfc7`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 364.5 KB (364474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6be91d2a668f124038a4b58fd4ea66112de7b5b0b97a139693dfad7af569f`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2113532490862d3f6fbbc444054df6a45ac27fd7df836514bba886616282d1e`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed759800fa7e1df988ee6bd77b70fb0ff86c479116b939808e48316290b16876`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 19.8 MB (19826177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8359603b2119f0fa8a6571abae59b6fedadab69d593491f5654da2369da6101`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8691616fbb1ac24ed70ed40459202a0890dc879db4b4bd145bf682fe91a5f35d`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fede937bf0332135d9e85cd74b71cdabff018cd49fdb00377c1c8b6a955a98`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df182fa0d8efc357ce076453fa75808da26e64d896888a663012d878865f2516`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.8 MB (22756719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662cc6465c91f282c1f13da905ddbb3283da516701570a3ba3bbee34f45732ee`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ce90bd08504a907b943a9371e9bc6cee33b2bfce11817ab311fde6581cf9a6`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afc5eb0fd1f12683a0f679fa6e3e6ec671d4c5216693af8d75aae719eb8775f`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab8c7824ed6e25645587020a647c04eb9024db067d572ea1afed4d07eb063a`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.3 MB (22301399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:8b2723933f4e20b03d82fad4f272979c45d21e29d5d5437a257dddd7a19b69e9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216826173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad7864511de6cf197875bc99d7c27cee1e5e4a9511cdb529bf075ad6e87eed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 18 Mar 2025 17:52:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:53:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:53:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:53:59 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:54:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:54:10 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:54:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efae6d46cdd88fc96e587336604ae353dae631d3edfb17299749b56f042f86e`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabff009c2b284cea2d40695c1b44d8b2e2b9a499dca58e92884fc4c4139d19b`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 338.8 KB (338767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299a5346171e96e11bbf7e75d2c923c9e767db919ae268e6303f0a8b51505132`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5681385a5fb68fbaf1d531ba43ef1a4eebca86ff9357c638c2b7ab8722096c`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bf621533bae634d522d1baa809d4030a69957056c545455ed8a6b54a582f37`  
		Last Modified: Tue, 18 Mar 2025 17:54:28 GMT  
		Size: 19.8 MB (19814343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d74b41781047bb821590370c205f708cb1312ac611cf3ffa7d92817cb3385`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8fd088b8dce22bb00a6dae4b3c11ff824bc93bbd5375cf39d193367b61b418`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c212d22018c8ed56b082699241fba4b6a975dcc80941663d3333e79726ef710`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120f89b8213b7712056cc20c3454b43dfbefee8092827722ba2bd7183f6693ea`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.7 MB (22744744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbe59c92ae308cc1ca95460830da582ea729bd502e6fdcc9e91a0980a0cf7f0`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24199190c27c55807d7aa76cacb9f25e09fbcbaf0385f92d8088eed73e875917`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f962b02a3d44056e12be508848bc41eb716d98ca72374c1e979fbcd1cf7c7`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ac0a28f0cff7f101228c34c93dbaf640a640f1ee5472053393f4931082d129`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.3 MB (22281907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:c780cf7ac1c5c0cb9599b2df0349dc29186be36aae111d30e399c208f227ae72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:8b2723933f4e20b03d82fad4f272979c45d21e29d5d5437a257dddd7a19b69e9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216826173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad7864511de6cf197875bc99d7c27cee1e5e4a9511cdb529bf075ad6e87eed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 18 Mar 2025 17:52:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:53:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:53:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:53:59 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:54:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:54:10 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:54:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efae6d46cdd88fc96e587336604ae353dae631d3edfb17299749b56f042f86e`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabff009c2b284cea2d40695c1b44d8b2e2b9a499dca58e92884fc4c4139d19b`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 338.8 KB (338767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299a5346171e96e11bbf7e75d2c923c9e767db919ae268e6303f0a8b51505132`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5681385a5fb68fbaf1d531ba43ef1a4eebca86ff9357c638c2b7ab8722096c`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bf621533bae634d522d1baa809d4030a69957056c545455ed8a6b54a582f37`  
		Last Modified: Tue, 18 Mar 2025 17:54:28 GMT  
		Size: 19.8 MB (19814343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d74b41781047bb821590370c205f708cb1312ac611cf3ffa7d92817cb3385`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8fd088b8dce22bb00a6dae4b3c11ff824bc93bbd5375cf39d193367b61b418`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c212d22018c8ed56b082699241fba4b6a975dcc80941663d3333e79726ef710`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120f89b8213b7712056cc20c3454b43dfbefee8092827722ba2bd7183f6693ea`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.7 MB (22744744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbe59c92ae308cc1ca95460830da582ea729bd502e6fdcc9e91a0980a0cf7f0`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24199190c27c55807d7aa76cacb9f25e09fbcbaf0385f92d8088eed73e875917`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f962b02a3d44056e12be508848bc41eb716d98ca72374c1e979fbcd1cf7c7`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ac0a28f0cff7f101228c34c93dbaf640a640f1ee5472053393f4931082d129`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.3 MB (22281907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:1602a0714e35d9428df55b3574afa737262d7899f2981edad083d6958065b422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:28.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:83ff96ddbee1bd02aa91285b3bf9690d98b899aff79585b714f4db4fa5fffcc7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335201497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a81d38ebdc303a8a3364a74efe23a1bedf44c1d7b8e6eed9a8be08f2556ec27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 18 Mar 2025 17:48:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:18 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:48:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:48:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:28 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:48:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:48:30 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:48:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:48:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:48:41 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:48:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f078092de8abb6d57d53e680c3076c9ef2bfbbf71c6f4a21348b227be48e4`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf4f863fc1275088515214a01de99ac68d3bfe956ba35597d3baa916414bfc7`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 364.5 KB (364474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6be91d2a668f124038a4b58fd4ea66112de7b5b0b97a139693dfad7af569f`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2113532490862d3f6fbbc444054df6a45ac27fd7df836514bba886616282d1e`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed759800fa7e1df988ee6bd77b70fb0ff86c479116b939808e48316290b16876`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 19.8 MB (19826177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8359603b2119f0fa8a6571abae59b6fedadab69d593491f5654da2369da6101`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8691616fbb1ac24ed70ed40459202a0890dc879db4b4bd145bf682fe91a5f35d`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fede937bf0332135d9e85cd74b71cdabff018cd49fdb00377c1c8b6a955a98`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df182fa0d8efc357ce076453fa75808da26e64d896888a663012d878865f2516`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.8 MB (22756719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662cc6465c91f282c1f13da905ddbb3283da516701570a3ba3bbee34f45732ee`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ce90bd08504a907b943a9371e9bc6cee33b2bfce11817ab311fde6581cf9a6`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afc5eb0fd1f12683a0f679fa6e3e6ec671d4c5216693af8d75aae719eb8775f`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab8c7824ed6e25645587020a647c04eb9024db067d572ea1afed4d07eb063a`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.3 MB (22301399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:4c2d528f844dac99062dc79967dd48348177d2db9ea7c66e86dd29010b571301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:28.0-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:81996f945dd6afd17a2f454f627cc9301a6d669d579eee88075c6866592b7eac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974045827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90411219e91a7a2282d6bafa1fa9f88374b9cc7fc5023a00346072afe20d252f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 18 Mar 2025 17:48:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:59 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:49:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:49:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:13 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:49:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:49:15 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:49:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:49:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:49:28 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:49:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0cd020c6471f62220ad8ed2ae2b3772b806f467cb0f11bc4308b9f2d0d26a`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cf4955d1aad1f83447efbdbcf08c9bd7423c84e7c6ac5bc6a5625140c991e0`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 400.2 KB (400166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90786f2c40deca413eed711fbbeb0abe197cababcf2e8b187fda5466bf3f9e14`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684238c758b95728bef5bbcf3815bce65fcb21040c3ec400e17b2e4b2975988`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7eac4b401484a405d9d595d4ab1ab2e2fa8f1dc11da64e453e0d575e376817`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 19.9 MB (19862606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68379e676f653db1ef6496f93f7f34f94e2e6adc3897f119f4d93a2092313f0`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df3c74807df3393363f62fd1b3dec83fe3a43f74559b92815cd5cbd580fbe6f`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5332d7c8bb3be4f3f08437752f48d8a66371aad10f5328510eeaa532db9383ba`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebe5ad6be9c69cb89a53b45d42605e0654403950049245df6ed82d6552beb2`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.8 MB (22789480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7945eb3de2b551bb141ecdcf88f5508c82ba67aa0f4910a08e9833a279946fde`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32749cc1ae150ad64cd11025c4de890ad6f72d84ccb8714200245b156bf136d1`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598bafa4dd3f7f04b9861f17341c80a693efdf2c84a11ab664533e4b3c2334b2`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b541b6491c1b4a89b6665a2775f4c706b4f2d8349747d04f83ac14f4ac23ca`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.3 MB (22334051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.1`

```console
$ docker pull docker@sha256:828290aa6d563454a849d59ca1bdfb14804679fa96ac0ba8eeabd76ee73c145d
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

### `docker:28.0.1` - linux; amd64

```console
$ docker pull docker@sha256:6f284d567aabce6fc59489d515b32e9e9e3c434d56a30a5bb4c78e31f8ce4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141423867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ebdb25d1582b57307f7586f07df28009b8bfe0ccafff9ccf38d2ece7e6142d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:b14dff50fdd36d583da1a62ad48743534c80d36636deb306ef3ea726fcc631b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c0320c0a080ec3869c570d9dcd47939db272e83fe901841e581fddfb923ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff3751a52465c2f4ca6f364704b34afeadb9a193f007f86b91faabe58e430298`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:66ed15e7c3455a7bd74e92449060237f9e6cd0c4a930a26cd8a90d344b555c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132050936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3635197fd3d2349cbe43887a8904a6cedcff1a4671bba7cab1a281c3bdaa98b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a710f976bef50357a64879fea6e83351c1d0ef59c4b2e03ab5c02c7d00693a`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 7.0 MB (7036932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd6d7147ebc3737f9054c3a2e0840f16cffd6eeb6d8050c84083e4f7c861189`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138ea4c8ade2ab710ebb4bf11c9a449e034a7623fc36ec4bf53cd7b4684cf96`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782343db207d529a26e6e14f1fe6094ba3881b7f186aa414619c6b0bd66a1a0d`  
		Last Modified: Tue, 18 Mar 2025 18:00:57 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c807da6e0bc19d88df1dcffa2ff2eb50eafca7dceb2b0c24a05d2e47f3792`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b099078ed89a269a48bb93f33b013c288941cf91ef7a9820fc61f2dccc973f5`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:737cf84ed7a67e9cbdcd7f70938e322e7cbbfb25319bca652b06940f188c2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ad73c0f54384a2fa3d6fb5a46a9eb39b0b72913cba768969303ee5f7b93452`

```dockerfile
```

-	Layers:
	-	`sha256:4e103ade0760fb22db55fb6f3af4aa1562af7fc301a00a074ed879630b63525f`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:05883987356d7f2b28e785e0c98411791033e75c7594688eb66d1a0db75a892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130382942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc322d32470857db2fae3bcdcd6f94fa963581539b2bb5205ccd14009f56f816`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04248460f4f43dda114cf6e38bd72647f90344cc42043161295d8a77bb78f15a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 6.4 MB (6366336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248db7df30a00f0d2a17263b4f5d6b39ac19a2f086f95f1f7ee5181fbd6ff1a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7413c171635e268ad441559ac341509383d0976e68d8a2e9db87346c6d946e2`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2143b75dc215725319c90f47ba313cdbf7f5122e30ddb6f234dd5b6a770d`  
		Last Modified: Fri, 14 Mar 2025 21:11:59 GMT  
		Size: 55.6 MB (55593647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266db4b4f66e90d74f43dd7ded419a89c5a9e048191be6e81055e0e03d3f3a5a`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8cc5b9a67b353b2df6581e3a544618582ca576f2d7c79d45b87fb4ba98477`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:4a44e37e075a395cc4355a8aa3064dab865c450125c889f99cb5a8f470bf5bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d583b2c788713970578b9a323504d5586eec6c267e185a0b04bda8960c932fcb`

```dockerfile
```

-	Layers:
	-	`sha256:7e5ffd9071082203139db743e85aa7abfe2b617598eac876a4750cd6c30d3d8e`  
		Last Modified: Fri, 14 Mar 2025 21:11:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18846793853859ff87551bfc02c1ab4fb4bde786d6d46b87560be2e79e44c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132776864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c214e95d979948c88a170436f1ccac8784a86409f26db755cf9d2f70e8855d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820b82ff2c20ecc51faaa7954e0192ce1942c3e6bfd6c173d46cad0bcc80149`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 7.0 MB (6978857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9890e98c90e9be8547535746a1ce2ac835b9625992bb48bda3a6e519e59d941c`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0e0fb9ff9ad6077e9d11b776646112fff92c378d559ec25f96dcf382ec7516`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a8d5e617c46c4d436d58a462243b20e345b0b8dd62e6779a4dc38aaf3e995`  
		Last Modified: Wed, 19 Mar 2025 03:00:55 GMT  
		Size: 55.6 MB (55566422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ea02a3cc4e3e276ac3b3d2b23dc7379c994e36bb72c3503b009dd59a1fbe`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813784e7a533f0caa2d0e0215db30009c1516ebd5e23cc60655e83bd8b598260`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:254eb39d6d9f390c0125b2ca271f80deb85fe0c535d6ef6fb7f1672319809a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e9357138bca17b2f423400bdaffc1e096dcd4778dc7cfd21592e5a5b7f339`

```dockerfile
```

-	Layers:
	-	`sha256:d8091161332ca59b3d16e344df59f9a3dae230a3ea1d0703d8c69e415a02c8d8`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-alpine3.21`

```console
$ docker pull docker@sha256:828290aa6d563454a849d59ca1bdfb14804679fa96ac0ba8eeabd76ee73c145d
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

### `docker:28.0.1-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:6f284d567aabce6fc59489d515b32e9e9e3c434d56a30a5bb4c78e31f8ce4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141423867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ebdb25d1582b57307f7586f07df28009b8bfe0ccafff9ccf38d2ece7e6142d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:b14dff50fdd36d583da1a62ad48743534c80d36636deb306ef3ea726fcc631b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c0320c0a080ec3869c570d9dcd47939db272e83fe901841e581fddfb923ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff3751a52465c2f4ca6f364704b34afeadb9a193f007f86b91faabe58e430298`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:66ed15e7c3455a7bd74e92449060237f9e6cd0c4a930a26cd8a90d344b555c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132050936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3635197fd3d2349cbe43887a8904a6cedcff1a4671bba7cab1a281c3bdaa98b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a710f976bef50357a64879fea6e83351c1d0ef59c4b2e03ab5c02c7d00693a`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 7.0 MB (7036932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd6d7147ebc3737f9054c3a2e0840f16cffd6eeb6d8050c84083e4f7c861189`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138ea4c8ade2ab710ebb4bf11c9a449e034a7623fc36ec4bf53cd7b4684cf96`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782343db207d529a26e6e14f1fe6094ba3881b7f186aa414619c6b0bd66a1a0d`  
		Last Modified: Tue, 18 Mar 2025 18:00:57 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c807da6e0bc19d88df1dcffa2ff2eb50eafca7dceb2b0c24a05d2e47f3792`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b099078ed89a269a48bb93f33b013c288941cf91ef7a9820fc61f2dccc973f5`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:737cf84ed7a67e9cbdcd7f70938e322e7cbbfb25319bca652b06940f188c2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ad73c0f54384a2fa3d6fb5a46a9eb39b0b72913cba768969303ee5f7b93452`

```dockerfile
```

-	Layers:
	-	`sha256:4e103ade0760fb22db55fb6f3af4aa1562af7fc301a00a074ed879630b63525f`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:05883987356d7f2b28e785e0c98411791033e75c7594688eb66d1a0db75a892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130382942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc322d32470857db2fae3bcdcd6f94fa963581539b2bb5205ccd14009f56f816`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04248460f4f43dda114cf6e38bd72647f90344cc42043161295d8a77bb78f15a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 6.4 MB (6366336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248db7df30a00f0d2a17263b4f5d6b39ac19a2f086f95f1f7ee5181fbd6ff1a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7413c171635e268ad441559ac341509383d0976e68d8a2e9db87346c6d946e2`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2143b75dc215725319c90f47ba313cdbf7f5122e30ddb6f234dd5b6a770d`  
		Last Modified: Fri, 14 Mar 2025 21:11:59 GMT  
		Size: 55.6 MB (55593647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266db4b4f66e90d74f43dd7ded419a89c5a9e048191be6e81055e0e03d3f3a5a`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8cc5b9a67b353b2df6581e3a544618582ca576f2d7c79d45b87fb4ba98477`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4a44e37e075a395cc4355a8aa3064dab865c450125c889f99cb5a8f470bf5bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d583b2c788713970578b9a323504d5586eec6c267e185a0b04bda8960c932fcb`

```dockerfile
```

-	Layers:
	-	`sha256:7e5ffd9071082203139db743e85aa7abfe2b617598eac876a4750cd6c30d3d8e`  
		Last Modified: Fri, 14 Mar 2025 21:11:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18846793853859ff87551bfc02c1ab4fb4bde786d6d46b87560be2e79e44c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132776864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c214e95d979948c88a170436f1ccac8784a86409f26db755cf9d2f70e8855d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820b82ff2c20ecc51faaa7954e0192ce1942c3e6bfd6c173d46cad0bcc80149`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 7.0 MB (6978857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9890e98c90e9be8547535746a1ce2ac835b9625992bb48bda3a6e519e59d941c`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0e0fb9ff9ad6077e9d11b776646112fff92c378d559ec25f96dcf382ec7516`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a8d5e617c46c4d436d58a462243b20e345b0b8dd62e6779a4dc38aaf3e995`  
		Last Modified: Wed, 19 Mar 2025 03:00:55 GMT  
		Size: 55.6 MB (55566422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ea02a3cc4e3e276ac3b3d2b23dc7379c994e36bb72c3503b009dd59a1fbe`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813784e7a533f0caa2d0e0215db30009c1516ebd5e23cc60655e83bd8b598260`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:254eb39d6d9f390c0125b2ca271f80deb85fe0c535d6ef6fb7f1672319809a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e9357138bca17b2f423400bdaffc1e096dcd4778dc7cfd21592e5a5b7f339`

```dockerfile
```

-	Layers:
	-	`sha256:d8091161332ca59b3d16e344df59f9a3dae230a3ea1d0703d8c69e415a02c8d8`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-cli`

```console
$ docker pull docker@sha256:b0cc8f27d36a03d30570d69d76615b84e4040bb52fd9c819bcb5a9cf1808d45d
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

### `docker:28.0.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:043c259759666d273afa94a9c9175a87a11f16cde2f613f4c527e4395b703a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74401810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbbfa15156e45896ae0baa0291763d59cbe8e9197af9396b1ce4d1c3fa92030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:054d1a0f0d9a7354f4ebcd12afbbe2a9020155beaa0ec46770c789ccbf1c7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e93df1fe28f45f774c9bf9ae35f4ca1912f62366ff899cafd275a526941419`

```dockerfile
```

-	Layers:
	-	`sha256:bac4c3a563812a6f84462124d368a71f165d3ee1ef9df06d3da71b7cca36e7d9`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:2af701b2acf52ac01aabe3f7b24129785436531e6994b6d19a75101c844b2aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69324552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f31a9e113936d6381be6fa03f180d10952d7db5923ef4da1db2e5c4d6ffb1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5e3d207e61cde6b1bc54354f37f0fbad8172bfc2584f0f5b511d0c598048f59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d14fb837116a45283ffadd7317ab0232cd066d977df7dc75bbd371ef47aed6`

```dockerfile
```

-	Layers:
	-	`sha256:0f25bf12b560e48dc887224d3f73240586d2726286656f557d257939d0aacae9`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:864e73fbbf97b3b2a57c6e72d332b7837b6ded3a278d4afa9e6777ebb5cdd5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68330712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00ed249c6b9ebcf5f398e457732ab11d2d31d789efee2927f9a5768620aa4b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 14 Mar 2025 11:04:27 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_VERSION=28.0.1
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Mar 2025 11:04:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Mar 2025 11:04:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2771de0165116b84662621b6ab21c653fd5a0e831c19632d56c2ad6511494d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7851d828c5af33e7f3518d627ee1eacf702912106be4bc93686f5213d4df2c3`

```dockerfile
```

-	Layers:
	-	`sha256:d7499afa1d7e720c1256ad1d97d24ebfce4a0b527055d56306c4ee3390c73d24`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9c69cedb70e576809b1c4bb33946ad8d85529f61c03e4b8f4641ef2e2c12c13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70126294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71220c9f3c0d88be6dd15374a7cde12582c3decef4a2ad6ac4ee45b346fd333f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a846f337948335ee9c66b55db9f4242f141b62ed0ac940a7308b6234a44672f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a466e3dd4f8d4aacc72abf776fe2dfb6d6eb6906cb0c1dd8bcca331951704947`

```dockerfile
```

-	Layers:
	-	`sha256:337cad1d65245942e78863cb17cababc17db3c09293347e6e4ce59e58b6d2e1c`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-cli-alpine3.21`

```console
$ docker pull docker@sha256:b0cc8f27d36a03d30570d69d76615b84e4040bb52fd9c819bcb5a9cf1808d45d
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

### `docker:28.0.1-cli-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:043c259759666d273afa94a9c9175a87a11f16cde2f613f4c527e4395b703a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74401810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbbfa15156e45896ae0baa0291763d59cbe8e9197af9396b1ce4d1c3fa92030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:054d1a0f0d9a7354f4ebcd12afbbe2a9020155beaa0ec46770c789ccbf1c7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e93df1fe28f45f774c9bf9ae35f4ca1912f62366ff899cafd275a526941419`

```dockerfile
```

-	Layers:
	-	`sha256:bac4c3a563812a6f84462124d368a71f165d3ee1ef9df06d3da71b7cca36e7d9`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:2af701b2acf52ac01aabe3f7b24129785436531e6994b6d19a75101c844b2aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69324552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f31a9e113936d6381be6fa03f180d10952d7db5923ef4da1db2e5c4d6ffb1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:5e3d207e61cde6b1bc54354f37f0fbad8172bfc2584f0f5b511d0c598048f59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d14fb837116a45283ffadd7317ab0232cd066d977df7dc75bbd371ef47aed6`

```dockerfile
```

-	Layers:
	-	`sha256:0f25bf12b560e48dc887224d3f73240586d2726286656f557d257939d0aacae9`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:864e73fbbf97b3b2a57c6e72d332b7837b6ded3a278d4afa9e6777ebb5cdd5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68330712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00ed249c6b9ebcf5f398e457732ab11d2d31d789efee2927f9a5768620aa4b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 14 Mar 2025 11:04:27 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_VERSION=28.0.1
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Mar 2025 11:04:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Mar 2025 11:04:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:2771de0165116b84662621b6ab21c653fd5a0e831c19632d56c2ad6511494d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7851d828c5af33e7f3518d627ee1eacf702912106be4bc93686f5213d4df2c3`

```dockerfile
```

-	Layers:
	-	`sha256:d7499afa1d7e720c1256ad1d97d24ebfce4a0b527055d56306c4ee3390c73d24`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9c69cedb70e576809b1c4bb33946ad8d85529f61c03e4b8f4641ef2e2c12c13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70126294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71220c9f3c0d88be6dd15374a7cde12582c3decef4a2ad6ac4ee45b346fd333f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:a846f337948335ee9c66b55db9f4242f141b62ed0ac940a7308b6234a44672f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a466e3dd4f8d4aacc72abf776fe2dfb6d6eb6906cb0c1dd8bcca331951704947`

```dockerfile
```

-	Layers:
	-	`sha256:337cad1d65245942e78863cb17cababc17db3c09293347e6e4ce59e58b6d2e1c`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-dind`

```console
$ docker pull docker@sha256:828290aa6d563454a849d59ca1bdfb14804679fa96ac0ba8eeabd76ee73c145d
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

### `docker:28.0.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:6f284d567aabce6fc59489d515b32e9e9e3c434d56a30a5bb4c78e31f8ce4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141423867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ebdb25d1582b57307f7586f07df28009b8bfe0ccafff9ccf38d2ece7e6142d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b14dff50fdd36d583da1a62ad48743534c80d36636deb306ef3ea726fcc631b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c0320c0a080ec3869c570d9dcd47939db272e83fe901841e581fddfb923ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff3751a52465c2f4ca6f364704b34afeadb9a193f007f86b91faabe58e430298`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:66ed15e7c3455a7bd74e92449060237f9e6cd0c4a930a26cd8a90d344b555c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132050936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3635197fd3d2349cbe43887a8904a6cedcff1a4671bba7cab1a281c3bdaa98b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a710f976bef50357a64879fea6e83351c1d0ef59c4b2e03ab5c02c7d00693a`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 7.0 MB (7036932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd6d7147ebc3737f9054c3a2e0840f16cffd6eeb6d8050c84083e4f7c861189`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138ea4c8ade2ab710ebb4bf11c9a449e034a7623fc36ec4bf53cd7b4684cf96`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782343db207d529a26e6e14f1fe6094ba3881b7f186aa414619c6b0bd66a1a0d`  
		Last Modified: Tue, 18 Mar 2025 18:00:57 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c807da6e0bc19d88df1dcffa2ff2eb50eafca7dceb2b0c24a05d2e47f3792`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b099078ed89a269a48bb93f33b013c288941cf91ef7a9820fc61f2dccc973f5`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:737cf84ed7a67e9cbdcd7f70938e322e7cbbfb25319bca652b06940f188c2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ad73c0f54384a2fa3d6fb5a46a9eb39b0b72913cba768969303ee5f7b93452`

```dockerfile
```

-	Layers:
	-	`sha256:4e103ade0760fb22db55fb6f3af4aa1562af7fc301a00a074ed879630b63525f`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:05883987356d7f2b28e785e0c98411791033e75c7594688eb66d1a0db75a892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130382942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc322d32470857db2fae3bcdcd6f94fa963581539b2bb5205ccd14009f56f816`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04248460f4f43dda114cf6e38bd72647f90344cc42043161295d8a77bb78f15a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 6.4 MB (6366336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248db7df30a00f0d2a17263b4f5d6b39ac19a2f086f95f1f7ee5181fbd6ff1a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7413c171635e268ad441559ac341509383d0976e68d8a2e9db87346c6d946e2`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2143b75dc215725319c90f47ba313cdbf7f5122e30ddb6f234dd5b6a770d`  
		Last Modified: Fri, 14 Mar 2025 21:11:59 GMT  
		Size: 55.6 MB (55593647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266db4b4f66e90d74f43dd7ded419a89c5a9e048191be6e81055e0e03d3f3a5a`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8cc5b9a67b353b2df6581e3a544618582ca576f2d7c79d45b87fb4ba98477`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4a44e37e075a395cc4355a8aa3064dab865c450125c889f99cb5a8f470bf5bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d583b2c788713970578b9a323504d5586eec6c267e185a0b04bda8960c932fcb`

```dockerfile
```

-	Layers:
	-	`sha256:7e5ffd9071082203139db743e85aa7abfe2b617598eac876a4750cd6c30d3d8e`  
		Last Modified: Fri, 14 Mar 2025 21:11:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18846793853859ff87551bfc02c1ab4fb4bde786d6d46b87560be2e79e44c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132776864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c214e95d979948c88a170436f1ccac8784a86409f26db755cf9d2f70e8855d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820b82ff2c20ecc51faaa7954e0192ce1942c3e6bfd6c173d46cad0bcc80149`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 7.0 MB (6978857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9890e98c90e9be8547535746a1ce2ac835b9625992bb48bda3a6e519e59d941c`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0e0fb9ff9ad6077e9d11b776646112fff92c378d559ec25f96dcf382ec7516`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a8d5e617c46c4d436d58a462243b20e345b0b8dd62e6779a4dc38aaf3e995`  
		Last Modified: Wed, 19 Mar 2025 03:00:55 GMT  
		Size: 55.6 MB (55566422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ea02a3cc4e3e276ac3b3d2b23dc7379c994e36bb72c3503b009dd59a1fbe`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813784e7a533f0caa2d0e0215db30009c1516ebd5e23cc60655e83bd8b598260`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:254eb39d6d9f390c0125b2ca271f80deb85fe0c535d6ef6fb7f1672319809a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e9357138bca17b2f423400bdaffc1e096dcd4778dc7cfd21592e5a5b7f339`

```dockerfile
```

-	Layers:
	-	`sha256:d8091161332ca59b3d16e344df59f9a3dae230a3ea1d0703d8c69e415a02c8d8`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-dind-alpine3.21`

```console
$ docker pull docker@sha256:828290aa6d563454a849d59ca1bdfb14804679fa96ac0ba8eeabd76ee73c145d
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

### `docker:28.0.1-dind-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:6f284d567aabce6fc59489d515b32e9e9e3c434d56a30a5bb4c78e31f8ce4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141423867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ebdb25d1582b57307f7586f07df28009b8bfe0ccafff9ccf38d2ece7e6142d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:b14dff50fdd36d583da1a62ad48743534c80d36636deb306ef3ea726fcc631b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c0320c0a080ec3869c570d9dcd47939db272e83fe901841e581fddfb923ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff3751a52465c2f4ca6f364704b34afeadb9a193f007f86b91faabe58e430298`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:66ed15e7c3455a7bd74e92449060237f9e6cd0c4a930a26cd8a90d344b555c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132050936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3635197fd3d2349cbe43887a8904a6cedcff1a4671bba7cab1a281c3bdaa98b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a710f976bef50357a64879fea6e83351c1d0ef59c4b2e03ab5c02c7d00693a`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 7.0 MB (7036932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd6d7147ebc3737f9054c3a2e0840f16cffd6eeb6d8050c84083e4f7c861189`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138ea4c8ade2ab710ebb4bf11c9a449e034a7623fc36ec4bf53cd7b4684cf96`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782343db207d529a26e6e14f1fe6094ba3881b7f186aa414619c6b0bd66a1a0d`  
		Last Modified: Tue, 18 Mar 2025 18:00:57 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c807da6e0bc19d88df1dcffa2ff2eb50eafca7dceb2b0c24a05d2e47f3792`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b099078ed89a269a48bb93f33b013c288941cf91ef7a9820fc61f2dccc973f5`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:737cf84ed7a67e9cbdcd7f70938e322e7cbbfb25319bca652b06940f188c2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ad73c0f54384a2fa3d6fb5a46a9eb39b0b72913cba768969303ee5f7b93452`

```dockerfile
```

-	Layers:
	-	`sha256:4e103ade0760fb22db55fb6f3af4aa1562af7fc301a00a074ed879630b63525f`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:05883987356d7f2b28e785e0c98411791033e75c7594688eb66d1a0db75a892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130382942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc322d32470857db2fae3bcdcd6f94fa963581539b2bb5205ccd14009f56f816`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04248460f4f43dda114cf6e38bd72647f90344cc42043161295d8a77bb78f15a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 6.4 MB (6366336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248db7df30a00f0d2a17263b4f5d6b39ac19a2f086f95f1f7ee5181fbd6ff1a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7413c171635e268ad441559ac341509383d0976e68d8a2e9db87346c6d946e2`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2143b75dc215725319c90f47ba313cdbf7f5122e30ddb6f234dd5b6a770d`  
		Last Modified: Fri, 14 Mar 2025 21:11:59 GMT  
		Size: 55.6 MB (55593647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266db4b4f66e90d74f43dd7ded419a89c5a9e048191be6e81055e0e03d3f3a5a`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8cc5b9a67b353b2df6581e3a544618582ca576f2d7c79d45b87fb4ba98477`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4a44e37e075a395cc4355a8aa3064dab865c450125c889f99cb5a8f470bf5bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d583b2c788713970578b9a323504d5586eec6c267e185a0b04bda8960c932fcb`

```dockerfile
```

-	Layers:
	-	`sha256:7e5ffd9071082203139db743e85aa7abfe2b617598eac876a4750cd6c30d3d8e`  
		Last Modified: Fri, 14 Mar 2025 21:11:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18846793853859ff87551bfc02c1ab4fb4bde786d6d46b87560be2e79e44c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132776864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c214e95d979948c88a170436f1ccac8784a86409f26db755cf9d2f70e8855d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820b82ff2c20ecc51faaa7954e0192ce1942c3e6bfd6c173d46cad0bcc80149`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 7.0 MB (6978857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9890e98c90e9be8547535746a1ce2ac835b9625992bb48bda3a6e519e59d941c`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0e0fb9ff9ad6077e9d11b776646112fff92c378d559ec25f96dcf382ec7516`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a8d5e617c46c4d436d58a462243b20e345b0b8dd62e6779a4dc38aaf3e995`  
		Last Modified: Wed, 19 Mar 2025 03:00:55 GMT  
		Size: 55.6 MB (55566422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ea02a3cc4e3e276ac3b3d2b23dc7379c994e36bb72c3503b009dd59a1fbe`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813784e7a533f0caa2d0e0215db30009c1516ebd5e23cc60655e83bd8b598260`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:254eb39d6d9f390c0125b2ca271f80deb85fe0c535d6ef6fb7f1672319809a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e9357138bca17b2f423400bdaffc1e096dcd4778dc7cfd21592e5a5b7f339`

```dockerfile
```

-	Layers:
	-	`sha256:d8091161332ca59b3d16e344df59f9a3dae230a3ea1d0703d8c69e415a02c8d8`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-dind-rootless`

```console
$ docker pull docker@sha256:754aa7c1bfd9b5dad719015ad9357a0c7a66f3bde2c932b22ff1684357563eb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:32dfa25aad31337bd5141ba8380e0288c5aba973e0d1013d30cdd080ee500eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159578202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66f208fb1c578feb5ab1bbafb38911d9d47973065e3e2a8d5f7448be4c121c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8142c21eb3ac89c3e91203a0f16eb4cd39edb96ed809c12850cc330d6cdbea30`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 986.6 KB (986583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3424f6c492d784bb37beb7ab00c8b859ce13297717dc058ad18fe672c9ff69`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711170e2dc3314d2bc5e383d4df9bfeb3a49f7f56568960e8641335a124cc79`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d519ed6a081ab4200ce5e80dbea1046b066972f89c82dfe38ec962f51b7bec00`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 17.2 MB (17166411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd10a25c4410d07e25fcf12f7f25f5c8cb517a5b7be041a8c49574903667d34`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bcfeee32b0e1597300ac937a9a375e876a3ebf5644f4cfc31af89aa04e6cf1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843ea3c71e7950d1793b6c27c89054c2752811c275ea6a0c88ec2f47ad44c264`

```dockerfile
```

-	Layers:
	-	`sha256:0434e0329e64168242a488dc2ec087d57bbe6f29f380339d8b4c8a3e79e5bce6`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:19e4800a186f237d40cbcef2b6703bef220e7bc5c52f0df68845b5a65e50dbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153065629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e0d8637a09a7e5fc0e156a815f870279820b8f7c6bd846366df78e37aab5c7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de7b18622f97a3c1064dce569f3ff7a45ce5eefdf7e45c63fbe82ad6369360d`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 8.1 MB (8076411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e796aa6b98c5b6ef094554192c9676616631c209858d78a497ad8e57a085f1dc`  
		Last Modified: Fri, 14 Mar 2025 21:49:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cac35bcba55fd0892cfa0fd723ea433271f4a7bce0a06e6817a2278acd9aad7`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 18.4 MB (18425653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46c4ca48b2cb3e83a2c78785255753f121b7d03854e34c6d7c787ce45d8b60`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 20.0 MB (20040986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11e199ee8eacbea69e12a4fb23b40f68ea0b4f1ab759f2131291d19402cb3b`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 19.6 MB (19581878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dce91693c540282e494983ba2524586f9cd6b97f769eb795b4d852e7fdd581`  
		Last Modified: Fri, 14 Mar 2025 21:49:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438358ebfbee95af11c2bfbf1b71df6e9c81aace1fc12187b64c58aaf900d77e`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df88cc4d1057f2f914bc664a4b82a142b8dcf06a77e87a9516eae14364f033a4`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35dcd7757e18c2324a8fc638d2a9ea3e74daad9f8cc5877a2eaa68b7942c60`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 7.0 MB (6978811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69aeae86dcdffdf63366bcf9bbb61336fe9a67fcecbe8d29aa8b83b292002c`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 99.4 KB (99380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e216e0fa6851d219c9c6c2188ef5eab27b52103511d70e675d082ca22096e8`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2947322861bdc5f37e9119d204f26fd249623e0295d104af44bd1673c09a1663`  
		Last Modified: Fri, 14 Mar 2025 23:43:12 GMT  
		Size: 55.6 MB (55566453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170de84416a27698febebda6b66c8758b52aaa68d72775b3d83ca68f5561627f`  
		Last Modified: Fri, 14 Mar 2025 23:43:11 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa622cc428daff0de20c56abfa4b13ed8ea8323c3f1a30cd9c0f36b258be4aae`  
		Last Modified: Fri, 14 Mar 2025 23:43:11 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87d24bb402bee44662ae05f56a7f802abb4bfe4946eed38e6b92e30346bec96`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 1.0 MB (1014190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c69a48222fb6f42109b9a380dbfa4be336a0a0c016cd37d8619fae6835b85f`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64568427128fb5786c46527a81ed74941db093f35e996be0cf0d4ccba9f08482`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0ec1b2a82774ea69637c04bae551f0d327110921726fb1157674fe476b5a2`  
		Last Modified: Sat, 15 Mar 2025 00:10:32 GMT  
		Size: 19.3 MB (19279437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9574ada033fbed6c291f9ef3bc394ce883d5895ae06ae89797ddc2f3641de2e9`  
		Last Modified: Sat, 15 Mar 2025 00:10:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4537a5f78b6c74f3425552daffd342a3df407e99b582f9a04cc4edbe634b8ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ea771efeb5e1e724113f140d2fa43a5020ffd247c91f8542a8d7e3af0f08db`

```dockerfile
```

-	Layers:
	-	`sha256:c66d401445d485c1954b2c479641d5a36e9cd483c0110f40cab705706d4f2f3c`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-windowsservercore`

```console
$ docker pull docker@sha256:80ada8b5544018710daaf3e0df8c13fc9467ca8dab197647f5fb2011e476d13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0.1-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:81996f945dd6afd17a2f454f627cc9301a6d669d579eee88075c6866592b7eac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974045827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90411219e91a7a2282d6bafa1fa9f88374b9cc7fc5023a00346072afe20d252f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 18 Mar 2025 17:48:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:59 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:49:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:49:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:13 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:49:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:49:15 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:49:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:49:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:49:28 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:49:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0cd020c6471f62220ad8ed2ae2b3772b806f467cb0f11bc4308b9f2d0d26a`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cf4955d1aad1f83447efbdbcf08c9bd7423c84e7c6ac5bc6a5625140c991e0`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 400.2 KB (400166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90786f2c40deca413eed711fbbeb0abe197cababcf2e8b187fda5466bf3f9e14`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684238c758b95728bef5bbcf3815bce65fcb21040c3ec400e17b2e4b2975988`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7eac4b401484a405d9d595d4ab1ab2e2fa8f1dc11da64e453e0d575e376817`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 19.9 MB (19862606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68379e676f653db1ef6496f93f7f34f94e2e6adc3897f119f4d93a2092313f0`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df3c74807df3393363f62fd1b3dec83fe3a43f74559b92815cd5cbd580fbe6f`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5332d7c8bb3be4f3f08437752f48d8a66371aad10f5328510eeaa532db9383ba`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebe5ad6be9c69cb89a53b45d42605e0654403950049245df6ed82d6552beb2`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.8 MB (22789480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7945eb3de2b551bb141ecdcf88f5508c82ba67aa0f4910a08e9833a279946fde`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32749cc1ae150ad64cd11025c4de890ad6f72d84ccb8714200245b156bf136d1`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598bafa4dd3f7f04b9861f17341c80a693efdf2c84a11ab664533e4b3c2334b2`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b541b6491c1b4a89b6665a2775f4c706b4f2d8349747d04f83ac14f4ac23ca`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.3 MB (22334051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.1-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:83ff96ddbee1bd02aa91285b3bf9690d98b899aff79585b714f4db4fa5fffcc7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335201497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a81d38ebdc303a8a3364a74efe23a1bedf44c1d7b8e6eed9a8be08f2556ec27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 18 Mar 2025 17:48:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:18 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:48:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:48:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:28 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:48:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:48:30 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:48:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:48:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:48:41 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:48:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f078092de8abb6d57d53e680c3076c9ef2bfbbf71c6f4a21348b227be48e4`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf4f863fc1275088515214a01de99ac68d3bfe956ba35597d3baa916414bfc7`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 364.5 KB (364474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6be91d2a668f124038a4b58fd4ea66112de7b5b0b97a139693dfad7af569f`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2113532490862d3f6fbbc444054df6a45ac27fd7df836514bba886616282d1e`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed759800fa7e1df988ee6bd77b70fb0ff86c479116b939808e48316290b16876`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 19.8 MB (19826177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8359603b2119f0fa8a6571abae59b6fedadab69d593491f5654da2369da6101`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8691616fbb1ac24ed70ed40459202a0890dc879db4b4bd145bf682fe91a5f35d`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fede937bf0332135d9e85cd74b71cdabff018cd49fdb00377c1c8b6a955a98`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df182fa0d8efc357ce076453fa75808da26e64d896888a663012d878865f2516`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.8 MB (22756719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662cc6465c91f282c1f13da905ddbb3283da516701570a3ba3bbee34f45732ee`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ce90bd08504a907b943a9371e9bc6cee33b2bfce11817ab311fde6581cf9a6`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afc5eb0fd1f12683a0f679fa6e3e6ec671d4c5216693af8d75aae719eb8775f`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab8c7824ed6e25645587020a647c04eb9024db067d572ea1afed4d07eb063a`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.3 MB (22301399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.1-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:8b2723933f4e20b03d82fad4f272979c45d21e29d5d5437a257dddd7a19b69e9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216826173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad7864511de6cf197875bc99d7c27cee1e5e4a9511cdb529bf075ad6e87eed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 18 Mar 2025 17:52:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:53:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:53:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:53:59 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:54:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:54:10 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:54:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efae6d46cdd88fc96e587336604ae353dae631d3edfb17299749b56f042f86e`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabff009c2b284cea2d40695c1b44d8b2e2b9a499dca58e92884fc4c4139d19b`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 338.8 KB (338767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299a5346171e96e11bbf7e75d2c923c9e767db919ae268e6303f0a8b51505132`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5681385a5fb68fbaf1d531ba43ef1a4eebca86ff9357c638c2b7ab8722096c`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bf621533bae634d522d1baa809d4030a69957056c545455ed8a6b54a582f37`  
		Last Modified: Tue, 18 Mar 2025 17:54:28 GMT  
		Size: 19.8 MB (19814343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d74b41781047bb821590370c205f708cb1312ac611cf3ffa7d92817cb3385`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8fd088b8dce22bb00a6dae4b3c11ff824bc93bbd5375cf39d193367b61b418`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c212d22018c8ed56b082699241fba4b6a975dcc80941663d3333e79726ef710`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120f89b8213b7712056cc20c3454b43dfbefee8092827722ba2bd7183f6693ea`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.7 MB (22744744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbe59c92ae308cc1ca95460830da582ea729bd502e6fdcc9e91a0980a0cf7f0`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24199190c27c55807d7aa76cacb9f25e09fbcbaf0385f92d8088eed73e875917`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f962b02a3d44056e12be508848bc41eb716d98ca72374c1e979fbcd1cf7c7`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ac0a28f0cff7f101228c34c93dbaf640a640f1ee5472053393f4931082d129`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.3 MB (22281907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:c780cf7ac1c5c0cb9599b2df0349dc29186be36aae111d30e399c208f227ae72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0.1-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:8b2723933f4e20b03d82fad4f272979c45d21e29d5d5437a257dddd7a19b69e9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216826173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad7864511de6cf197875bc99d7c27cee1e5e4a9511cdb529bf075ad6e87eed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 18 Mar 2025 17:52:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:53:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:53:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:53:59 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:54:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:54:10 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:54:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efae6d46cdd88fc96e587336604ae353dae631d3edfb17299749b56f042f86e`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabff009c2b284cea2d40695c1b44d8b2e2b9a499dca58e92884fc4c4139d19b`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 338.8 KB (338767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299a5346171e96e11bbf7e75d2c923c9e767db919ae268e6303f0a8b51505132`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5681385a5fb68fbaf1d531ba43ef1a4eebca86ff9357c638c2b7ab8722096c`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bf621533bae634d522d1baa809d4030a69957056c545455ed8a6b54a582f37`  
		Last Modified: Tue, 18 Mar 2025 17:54:28 GMT  
		Size: 19.8 MB (19814343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d74b41781047bb821590370c205f708cb1312ac611cf3ffa7d92817cb3385`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8fd088b8dce22bb00a6dae4b3c11ff824bc93bbd5375cf39d193367b61b418`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c212d22018c8ed56b082699241fba4b6a975dcc80941663d3333e79726ef710`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120f89b8213b7712056cc20c3454b43dfbefee8092827722ba2bd7183f6693ea`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.7 MB (22744744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbe59c92ae308cc1ca95460830da582ea729bd502e6fdcc9e91a0980a0cf7f0`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24199190c27c55807d7aa76cacb9f25e09fbcbaf0385f92d8088eed73e875917`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f962b02a3d44056e12be508848bc41eb716d98ca72374c1e979fbcd1cf7c7`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ac0a28f0cff7f101228c34c93dbaf640a640f1ee5472053393f4931082d129`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.3 MB (22281907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:1602a0714e35d9428df55b3574afa737262d7899f2981edad083d6958065b422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:28.0.1-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:83ff96ddbee1bd02aa91285b3bf9690d98b899aff79585b714f4db4fa5fffcc7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335201497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a81d38ebdc303a8a3364a74efe23a1bedf44c1d7b8e6eed9a8be08f2556ec27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 18 Mar 2025 17:48:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:18 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:48:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:48:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:28 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:48:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:48:30 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:48:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:48:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:48:41 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:48:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f078092de8abb6d57d53e680c3076c9ef2bfbbf71c6f4a21348b227be48e4`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf4f863fc1275088515214a01de99ac68d3bfe956ba35597d3baa916414bfc7`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 364.5 KB (364474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6be91d2a668f124038a4b58fd4ea66112de7b5b0b97a139693dfad7af569f`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2113532490862d3f6fbbc444054df6a45ac27fd7df836514bba886616282d1e`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed759800fa7e1df988ee6bd77b70fb0ff86c479116b939808e48316290b16876`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 19.8 MB (19826177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8359603b2119f0fa8a6571abae59b6fedadab69d593491f5654da2369da6101`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8691616fbb1ac24ed70ed40459202a0890dc879db4b4bd145bf682fe91a5f35d`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fede937bf0332135d9e85cd74b71cdabff018cd49fdb00377c1c8b6a955a98`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df182fa0d8efc357ce076453fa75808da26e64d896888a663012d878865f2516`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.8 MB (22756719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662cc6465c91f282c1f13da905ddbb3283da516701570a3ba3bbee34f45732ee`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ce90bd08504a907b943a9371e9bc6cee33b2bfce11817ab311fde6581cf9a6`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afc5eb0fd1f12683a0f679fa6e3e6ec671d4c5216693af8d75aae719eb8775f`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab8c7824ed6e25645587020a647c04eb9024db067d572ea1afed4d07eb063a`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.3 MB (22301399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:4c2d528f844dac99062dc79967dd48348177d2db9ea7c66e86dd29010b571301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:28.0.1-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:81996f945dd6afd17a2f454f627cc9301a6d669d579eee88075c6866592b7eac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974045827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90411219e91a7a2282d6bafa1fa9f88374b9cc7fc5023a00346072afe20d252f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 18 Mar 2025 17:48:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:59 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:49:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:49:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:13 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:49:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:49:15 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:49:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:49:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:49:28 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:49:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0cd020c6471f62220ad8ed2ae2b3772b806f467cb0f11bc4308b9f2d0d26a`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cf4955d1aad1f83447efbdbcf08c9bd7423c84e7c6ac5bc6a5625140c991e0`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 400.2 KB (400166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90786f2c40deca413eed711fbbeb0abe197cababcf2e8b187fda5466bf3f9e14`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684238c758b95728bef5bbcf3815bce65fcb21040c3ec400e17b2e4b2975988`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7eac4b401484a405d9d595d4ab1ab2e2fa8f1dc11da64e453e0d575e376817`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 19.9 MB (19862606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68379e676f653db1ef6496f93f7f34f94e2e6adc3897f119f4d93a2092313f0`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df3c74807df3393363f62fd1b3dec83fe3a43f74559b92815cd5cbd580fbe6f`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5332d7c8bb3be4f3f08437752f48d8a66371aad10f5328510eeaa532db9383ba`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebe5ad6be9c69cb89a53b45d42605e0654403950049245df6ed82d6552beb2`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.8 MB (22789480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7945eb3de2b551bb141ecdcf88f5508c82ba67aa0f4910a08e9833a279946fde`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32749cc1ae150ad64cd11025c4de890ad6f72d84ccb8714200245b156bf136d1`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598bafa4dd3f7f04b9861f17341c80a693efdf2c84a11ab664533e4b3c2334b2`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b541b6491c1b4a89b6665a2775f4c706b4f2d8349747d04f83ac14f4ac23ca`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.3 MB (22334051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:b0cc8f27d36a03d30570d69d76615b84e4040bb52fd9c819bcb5a9cf1808d45d
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
$ docker pull docker@sha256:043c259759666d273afa94a9c9175a87a11f16cde2f613f4c527e4395b703a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74401810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbbfa15156e45896ae0baa0291763d59cbe8e9197af9396b1ce4d1c3fa92030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:054d1a0f0d9a7354f4ebcd12afbbe2a9020155beaa0ec46770c789ccbf1c7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e93df1fe28f45f774c9bf9ae35f4ca1912f62366ff899cafd275a526941419`

```dockerfile
```

-	Layers:
	-	`sha256:bac4c3a563812a6f84462124d368a71f165d3ee1ef9df06d3da71b7cca36e7d9`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:2af701b2acf52ac01aabe3f7b24129785436531e6994b6d19a75101c844b2aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69324552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f31a9e113936d6381be6fa03f180d10952d7db5923ef4da1db2e5c4d6ffb1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:5e3d207e61cde6b1bc54354f37f0fbad8172bfc2584f0f5b511d0c598048f59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d14fb837116a45283ffadd7317ab0232cd066d977df7dc75bbd371ef47aed6`

```dockerfile
```

-	Layers:
	-	`sha256:0f25bf12b560e48dc887224d3f73240586d2726286656f557d257939d0aacae9`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:864e73fbbf97b3b2a57c6e72d332b7837b6ded3a278d4afa9e6777ebb5cdd5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68330712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00ed249c6b9ebcf5f398e457732ab11d2d31d789efee2927f9a5768620aa4b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 14 Mar 2025 11:04:27 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_VERSION=28.0.1
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Fri, 14 Mar 2025 11:04:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Mar 2025 11:04:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Mar 2025 11:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Mar 2025 11:04:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:2771de0165116b84662621b6ab21c653fd5a0e831c19632d56c2ad6511494d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7851d828c5af33e7f3518d627ee1eacf702912106be4bc93686f5213d4df2c3`

```dockerfile
```

-	Layers:
	-	`sha256:d7499afa1d7e720c1256ad1d97d24ebfce4a0b527055d56306c4ee3390c73d24`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9c69cedb70e576809b1c4bb33946ad8d85529f61c03e4b8f4641ef2e2c12c13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70126294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71220c9f3c0d88be6dd15374a7cde12582c3decef4a2ad6ac4ee45b346fd333f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a846f337948335ee9c66b55db9f4242f141b62ed0ac940a7308b6234a44672f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a466e3dd4f8d4aacc72abf776fe2dfb6d6eb6906cb0c1dd8bcca331951704947`

```dockerfile
```

-	Layers:
	-	`sha256:337cad1d65245942e78863cb17cababc17db3c09293347e6e4ce59e58b6d2e1c`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:828290aa6d563454a849d59ca1bdfb14804679fa96ac0ba8eeabd76ee73c145d
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
$ docker pull docker@sha256:6f284d567aabce6fc59489d515b32e9e9e3c434d56a30a5bb4c78e31f8ce4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141423867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ebdb25d1582b57307f7586f07df28009b8bfe0ccafff9ccf38d2ece7e6142d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b14dff50fdd36d583da1a62ad48743534c80d36636deb306ef3ea726fcc631b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c0320c0a080ec3869c570d9dcd47939db272e83fe901841e581fddfb923ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff3751a52465c2f4ca6f364704b34afeadb9a193f007f86b91faabe58e430298`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:66ed15e7c3455a7bd74e92449060237f9e6cd0c4a930a26cd8a90d344b555c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132050936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3635197fd3d2349cbe43887a8904a6cedcff1a4671bba7cab1a281c3bdaa98b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a710f976bef50357a64879fea6e83351c1d0ef59c4b2e03ab5c02c7d00693a`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 7.0 MB (7036932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd6d7147ebc3737f9054c3a2e0840f16cffd6eeb6d8050c84083e4f7c861189`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138ea4c8ade2ab710ebb4bf11c9a449e034a7623fc36ec4bf53cd7b4684cf96`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782343db207d529a26e6e14f1fe6094ba3881b7f186aa414619c6b0bd66a1a0d`  
		Last Modified: Tue, 18 Mar 2025 18:00:57 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c807da6e0bc19d88df1dcffa2ff2eb50eafca7dceb2b0c24a05d2e47f3792`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b099078ed89a269a48bb93f33b013c288941cf91ef7a9820fc61f2dccc973f5`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:737cf84ed7a67e9cbdcd7f70938e322e7cbbfb25319bca652b06940f188c2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ad73c0f54384a2fa3d6fb5a46a9eb39b0b72913cba768969303ee5f7b93452`

```dockerfile
```

-	Layers:
	-	`sha256:4e103ade0760fb22db55fb6f3af4aa1562af7fc301a00a074ed879630b63525f`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:05883987356d7f2b28e785e0c98411791033e75c7594688eb66d1a0db75a892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130382942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc322d32470857db2fae3bcdcd6f94fa963581539b2bb5205ccd14009f56f816`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04248460f4f43dda114cf6e38bd72647f90344cc42043161295d8a77bb78f15a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 6.4 MB (6366336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248db7df30a00f0d2a17263b4f5d6b39ac19a2f086f95f1f7ee5181fbd6ff1a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7413c171635e268ad441559ac341509383d0976e68d8a2e9db87346c6d946e2`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2143b75dc215725319c90f47ba313cdbf7f5122e30ddb6f234dd5b6a770d`  
		Last Modified: Fri, 14 Mar 2025 21:11:59 GMT  
		Size: 55.6 MB (55593647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266db4b4f66e90d74f43dd7ded419a89c5a9e048191be6e81055e0e03d3f3a5a`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8cc5b9a67b353b2df6581e3a544618582ca576f2d7c79d45b87fb4ba98477`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:4a44e37e075a395cc4355a8aa3064dab865c450125c889f99cb5a8f470bf5bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d583b2c788713970578b9a323504d5586eec6c267e185a0b04bda8960c932fcb`

```dockerfile
```

-	Layers:
	-	`sha256:7e5ffd9071082203139db743e85aa7abfe2b617598eac876a4750cd6c30d3d8e`  
		Last Modified: Fri, 14 Mar 2025 21:11:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18846793853859ff87551bfc02c1ab4fb4bde786d6d46b87560be2e79e44c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132776864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c214e95d979948c88a170436f1ccac8784a86409f26db755cf9d2f70e8855d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820b82ff2c20ecc51faaa7954e0192ce1942c3e6bfd6c173d46cad0bcc80149`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 7.0 MB (6978857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9890e98c90e9be8547535746a1ce2ac835b9625992bb48bda3a6e519e59d941c`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0e0fb9ff9ad6077e9d11b776646112fff92c378d559ec25f96dcf382ec7516`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a8d5e617c46c4d436d58a462243b20e345b0b8dd62e6779a4dc38aaf3e995`  
		Last Modified: Wed, 19 Mar 2025 03:00:55 GMT  
		Size: 55.6 MB (55566422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ea02a3cc4e3e276ac3b3d2b23dc7379c994e36bb72c3503b009dd59a1fbe`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813784e7a533f0caa2d0e0215db30009c1516ebd5e23cc60655e83bd8b598260`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:254eb39d6d9f390c0125b2ca271f80deb85fe0c535d6ef6fb7f1672319809a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e9357138bca17b2f423400bdaffc1e096dcd4778dc7cfd21592e5a5b7f339`

```dockerfile
```

-	Layers:
	-	`sha256:d8091161332ca59b3d16e344df59f9a3dae230a3ea1d0703d8c69e415a02c8d8`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:754aa7c1bfd9b5dad719015ad9357a0c7a66f3bde2c932b22ff1684357563eb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:32dfa25aad31337bd5141ba8380e0288c5aba973e0d1013d30cdd080ee500eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159578202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66f208fb1c578feb5ab1bbafb38911d9d47973065e3e2a8d5f7448be4c121c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8142c21eb3ac89c3e91203a0f16eb4cd39edb96ed809c12850cc330d6cdbea30`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 986.6 KB (986583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3424f6c492d784bb37beb7ab00c8b859ce13297717dc058ad18fe672c9ff69`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711170e2dc3314d2bc5e383d4df9bfeb3a49f7f56568960e8641335a124cc79`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d519ed6a081ab4200ce5e80dbea1046b066972f89c82dfe38ec962f51b7bec00`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 17.2 MB (17166411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd10a25c4410d07e25fcf12f7f25f5c8cb517a5b7be041a8c49574903667d34`  
		Last Modified: Tue, 18 Mar 2025 18:09:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bcfeee32b0e1597300ac937a9a375e876a3ebf5644f4cfc31af89aa04e6cf1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843ea3c71e7950d1793b6c27c89054c2752811c275ea6a0c88ec2f47ad44c264`

```dockerfile
```

-	Layers:
	-	`sha256:0434e0329e64168242a488dc2ec087d57bbe6f29f380339d8b4c8a3e79e5bce6`  
		Last Modified: Tue, 18 Mar 2025 18:09:46 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:19e4800a186f237d40cbcef2b6703bef220e7bc5c52f0df68845b5a65e50dbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153065629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e0d8637a09a7e5fc0e156a815f870279820b8f7c6bd846366df78e37aab5c7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de7b18622f97a3c1064dce569f3ff7a45ce5eefdf7e45c63fbe82ad6369360d`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 8.1 MB (8076411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e796aa6b98c5b6ef094554192c9676616631c209858d78a497ad8e57a085f1dc`  
		Last Modified: Fri, 14 Mar 2025 21:49:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cac35bcba55fd0892cfa0fd723ea433271f4a7bce0a06e6817a2278acd9aad7`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 18.4 MB (18425653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46c4ca48b2cb3e83a2c78785255753f121b7d03854e34c6d7c787ce45d8b60`  
		Last Modified: Fri, 14 Mar 2025 21:49:50 GMT  
		Size: 20.0 MB (20040986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11e199ee8eacbea69e12a4fb23b40f68ea0b4f1ab759f2131291d19402cb3b`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 19.6 MB (19581878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dce91693c540282e494983ba2524586f9cd6b97f769eb795b4d852e7fdd581`  
		Last Modified: Fri, 14 Mar 2025 21:49:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438358ebfbee95af11c2bfbf1b71df6e9c81aace1fc12187b64c58aaf900d77e`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df88cc4d1057f2f914bc664a4b82a142b8dcf06a77e87a9516eae14364f033a4`  
		Last Modified: Fri, 14 Mar 2025 21:49:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35dcd7757e18c2324a8fc638d2a9ea3e74daad9f8cc5877a2eaa68b7942c60`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 7.0 MB (6978811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69aeae86dcdffdf63366bcf9bbb61336fe9a67fcecbe8d29aa8b83b292002c`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 99.4 KB (99380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e216e0fa6851d219c9c6c2188ef5eab27b52103511d70e675d082ca22096e8`  
		Last Modified: Fri, 14 Mar 2025 23:43:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2947322861bdc5f37e9119d204f26fd249623e0295d104af44bd1673c09a1663`  
		Last Modified: Fri, 14 Mar 2025 23:43:12 GMT  
		Size: 55.6 MB (55566453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170de84416a27698febebda6b66c8758b52aaa68d72775b3d83ca68f5561627f`  
		Last Modified: Fri, 14 Mar 2025 23:43:11 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa622cc428daff0de20c56abfa4b13ed8ea8323c3f1a30cd9c0f36b258be4aae`  
		Last Modified: Fri, 14 Mar 2025 23:43:11 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87d24bb402bee44662ae05f56a7f802abb4bfe4946eed38e6b92e30346bec96`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 1.0 MB (1014190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c69a48222fb6f42109b9a380dbfa4be336a0a0c016cd37d8619fae6835b85f`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64568427128fb5786c46527a81ed74941db093f35e996be0cf0d4ccba9f08482`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0ec1b2a82774ea69637c04bae551f0d327110921726fb1157674fe476b5a2`  
		Last Modified: Sat, 15 Mar 2025 00:10:32 GMT  
		Size: 19.3 MB (19279437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9574ada033fbed6c291f9ef3bc394ce883d5895ae06ae89797ddc2f3641de2e9`  
		Last Modified: Sat, 15 Mar 2025 00:10:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4537a5f78b6c74f3425552daffd342a3df407e99b582f9a04cc4edbe634b8ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ea771efeb5e1e724113f140d2fa43a5020ffd247c91f8542a8d7e3af0f08db`

```dockerfile
```

-	Layers:
	-	`sha256:c66d401445d485c1954b2c479641d5a36e9cd483c0110f40cab705706d4f2f3c`  
		Last Modified: Sat, 15 Mar 2025 00:10:31 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:828290aa6d563454a849d59ca1bdfb14804679fa96ac0ba8eeabd76ee73c145d
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
$ docker pull docker@sha256:6f284d567aabce6fc59489d515b32e9e9e3c434d56a30a5bb4c78e31f8ce4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141423867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ebdb25d1582b57307f7586f07df28009b8bfe0ccafff9ccf38d2ece7e6142d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cfe465450d552be1bf2deec710f3ba9e5deddf1260b964e96ec30d84c9ae54`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 6.7 MB (6733043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20cfa8ee62519cbbceb609e46a7b786cbb04a3d1c09b8be11f3ed8eda81f50`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757b49ecc78be23926c0747aeb531f0493905d9e1ff1828a2bab778b82bd06`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0f7eadfbf8ac90c34f6f0aa895602faf18cfa46b4717c5228ba2446aeff0f`  
		Last Modified: Tue, 18 Mar 2025 18:01:36 GMT  
		Size: 60.2 MB (60192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3360eb53da5590d3e3475e8edd04910945557e22950c714c5b064847d996`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3993a7be48539bcc6eeb555e61cf7c2779226ad415b71a991281ee3b2b057`  
		Last Modified: Tue, 18 Mar 2025 18:01:34 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:b14dff50fdd36d583da1a62ad48743534c80d36636deb306ef3ea726fcc631b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c0320c0a080ec3869c570d9dcd47939db272e83fe901841e581fddfb923ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff3751a52465c2f4ca6f364704b34afeadb9a193f007f86b91faabe58e430298`  
		Last Modified: Tue, 18 Mar 2025 18:01:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:66ed15e7c3455a7bd74e92449060237f9e6cd0c4a930a26cd8a90d344b555c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132050936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3635197fd3d2349cbe43887a8904a6cedcff1a4671bba7cab1a281c3bdaa98b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a710f976bef50357a64879fea6e83351c1d0ef59c4b2e03ab5c02c7d00693a`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 7.0 MB (7036932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd6d7147ebc3737f9054c3a2e0840f16cffd6eeb6d8050c84083e4f7c861189`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138ea4c8ade2ab710ebb4bf11c9a449e034a7623fc36ec4bf53cd7b4684cf96`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782343db207d529a26e6e14f1fe6094ba3881b7f186aa414619c6b0bd66a1a0d`  
		Last Modified: Tue, 18 Mar 2025 18:00:57 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c807da6e0bc19d88df1dcffa2ff2eb50eafca7dceb2b0c24a05d2e47f3792`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b099078ed89a269a48bb93f33b013c288941cf91ef7a9820fc61f2dccc973f5`  
		Last Modified: Tue, 18 Mar 2025 18:00:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:737cf84ed7a67e9cbdcd7f70938e322e7cbbfb25319bca652b06940f188c2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ad73c0f54384a2fa3d6fb5a46a9eb39b0b72913cba768969303ee5f7b93452`

```dockerfile
```

-	Layers:
	-	`sha256:4e103ade0760fb22db55fb6f3af4aa1562af7fc301a00a074ed879630b63525f`  
		Last Modified: Tue, 18 Mar 2025 18:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:05883987356d7f2b28e785e0c98411791033e75c7594688eb66d1a0db75a892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130382942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc322d32470857db2fae3bcdcd6f94fa963581539b2bb5205ccd14009f56f816`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04248460f4f43dda114cf6e38bd72647f90344cc42043161295d8a77bb78f15a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 6.4 MB (6366336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248db7df30a00f0d2a17263b4f5d6b39ac19a2f086f95f1f7ee5181fbd6ff1a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7413c171635e268ad441559ac341509383d0976e68d8a2e9db87346c6d946e2`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2143b75dc215725319c90f47ba313cdbf7f5122e30ddb6f234dd5b6a770d`  
		Last Modified: Fri, 14 Mar 2025 21:11:59 GMT  
		Size: 55.6 MB (55593647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266db4b4f66e90d74f43dd7ded419a89c5a9e048191be6e81055e0e03d3f3a5a`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8cc5b9a67b353b2df6581e3a544618582ca576f2d7c79d45b87fb4ba98477`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:4a44e37e075a395cc4355a8aa3064dab865c450125c889f99cb5a8f470bf5bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d583b2c788713970578b9a323504d5586eec6c267e185a0b04bda8960c932fcb`

```dockerfile
```

-	Layers:
	-	`sha256:7e5ffd9071082203139db743e85aa7abfe2b617598eac876a4750cd6c30d3d8e`  
		Last Modified: Fri, 14 Mar 2025 21:11:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18846793853859ff87551bfc02c1ab4fb4bde786d6d46b87560be2e79e44c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132776864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c214e95d979948c88a170436f1ccac8784a86409f26db755cf9d2f70e8855d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820b82ff2c20ecc51faaa7954e0192ce1942c3e6bfd6c173d46cad0bcc80149`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 7.0 MB (6978857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9890e98c90e9be8547535746a1ce2ac835b9625992bb48bda3a6e519e59d941c`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0e0fb9ff9ad6077e9d11b776646112fff92c378d559ec25f96dcf382ec7516`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a8d5e617c46c4d436d58a462243b20e345b0b8dd62e6779a4dc38aaf3e995`  
		Last Modified: Wed, 19 Mar 2025 03:00:55 GMT  
		Size: 55.6 MB (55566422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ea02a3cc4e3e276ac3b3d2b23dc7379c994e36bb72c3503b009dd59a1fbe`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813784e7a533f0caa2d0e0215db30009c1516ebd5e23cc60655e83bd8b598260`  
		Last Modified: Wed, 19 Mar 2025 03:00:54 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:254eb39d6d9f390c0125b2ca271f80deb85fe0c535d6ef6fb7f1672319809a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e9357138bca17b2f423400bdaffc1e096dcd4778dc7cfd21592e5a5b7f339`

```dockerfile
```

-	Layers:
	-	`sha256:d8091161332ca59b3d16e344df59f9a3dae230a3ea1d0703d8c69e415a02c8d8`  
		Last Modified: Wed, 19 Mar 2025 03:00:53 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:80ada8b5544018710daaf3e0df8c13fc9467ca8dab197647f5fb2011e476d13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:81996f945dd6afd17a2f454f627cc9301a6d669d579eee88075c6866592b7eac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974045827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90411219e91a7a2282d6bafa1fa9f88374b9cc7fc5023a00346072afe20d252f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 18 Mar 2025 17:48:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:59 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:49:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:49:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:13 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:49:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:49:15 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:49:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:49:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:49:28 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:49:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0cd020c6471f62220ad8ed2ae2b3772b806f467cb0f11bc4308b9f2d0d26a`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cf4955d1aad1f83447efbdbcf08c9bd7423c84e7c6ac5bc6a5625140c991e0`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 400.2 KB (400166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90786f2c40deca413eed711fbbeb0abe197cababcf2e8b187fda5466bf3f9e14`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684238c758b95728bef5bbcf3815bce65fcb21040c3ec400e17b2e4b2975988`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7eac4b401484a405d9d595d4ab1ab2e2fa8f1dc11da64e453e0d575e376817`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 19.9 MB (19862606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68379e676f653db1ef6496f93f7f34f94e2e6adc3897f119f4d93a2092313f0`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df3c74807df3393363f62fd1b3dec83fe3a43f74559b92815cd5cbd580fbe6f`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5332d7c8bb3be4f3f08437752f48d8a66371aad10f5328510eeaa532db9383ba`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebe5ad6be9c69cb89a53b45d42605e0654403950049245df6ed82d6552beb2`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.8 MB (22789480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7945eb3de2b551bb141ecdcf88f5508c82ba67aa0f4910a08e9833a279946fde`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32749cc1ae150ad64cd11025c4de890ad6f72d84ccb8714200245b156bf136d1`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598bafa4dd3f7f04b9861f17341c80a693efdf2c84a11ab664533e4b3c2334b2`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b541b6491c1b4a89b6665a2775f4c706b4f2d8349747d04f83ac14f4ac23ca`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.3 MB (22334051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:83ff96ddbee1bd02aa91285b3bf9690d98b899aff79585b714f4db4fa5fffcc7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335201497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a81d38ebdc303a8a3364a74efe23a1bedf44c1d7b8e6eed9a8be08f2556ec27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 18 Mar 2025 17:48:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:18 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:48:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:48:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:28 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:48:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:48:30 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:48:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:48:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:48:41 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:48:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f078092de8abb6d57d53e680c3076c9ef2bfbbf71c6f4a21348b227be48e4`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf4f863fc1275088515214a01de99ac68d3bfe956ba35597d3baa916414bfc7`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 364.5 KB (364474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6be91d2a668f124038a4b58fd4ea66112de7b5b0b97a139693dfad7af569f`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2113532490862d3f6fbbc444054df6a45ac27fd7df836514bba886616282d1e`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed759800fa7e1df988ee6bd77b70fb0ff86c479116b939808e48316290b16876`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 19.8 MB (19826177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8359603b2119f0fa8a6571abae59b6fedadab69d593491f5654da2369da6101`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8691616fbb1ac24ed70ed40459202a0890dc879db4b4bd145bf682fe91a5f35d`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fede937bf0332135d9e85cd74b71cdabff018cd49fdb00377c1c8b6a955a98`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df182fa0d8efc357ce076453fa75808da26e64d896888a663012d878865f2516`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.8 MB (22756719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662cc6465c91f282c1f13da905ddbb3283da516701570a3ba3bbee34f45732ee`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ce90bd08504a907b943a9371e9bc6cee33b2bfce11817ab311fde6581cf9a6`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afc5eb0fd1f12683a0f679fa6e3e6ec671d4c5216693af8d75aae719eb8775f`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab8c7824ed6e25645587020a647c04eb9024db067d572ea1afed4d07eb063a`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.3 MB (22301399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:8b2723933f4e20b03d82fad4f272979c45d21e29d5d5437a257dddd7a19b69e9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216826173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad7864511de6cf197875bc99d7c27cee1e5e4a9511cdb529bf075ad6e87eed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 18 Mar 2025 17:52:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:53:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:53:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:53:59 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:54:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:54:10 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:54:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efae6d46cdd88fc96e587336604ae353dae631d3edfb17299749b56f042f86e`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabff009c2b284cea2d40695c1b44d8b2e2b9a499dca58e92884fc4c4139d19b`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 338.8 KB (338767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299a5346171e96e11bbf7e75d2c923c9e767db919ae268e6303f0a8b51505132`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5681385a5fb68fbaf1d531ba43ef1a4eebca86ff9357c638c2b7ab8722096c`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bf621533bae634d522d1baa809d4030a69957056c545455ed8a6b54a582f37`  
		Last Modified: Tue, 18 Mar 2025 17:54:28 GMT  
		Size: 19.8 MB (19814343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d74b41781047bb821590370c205f708cb1312ac611cf3ffa7d92817cb3385`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8fd088b8dce22bb00a6dae4b3c11ff824bc93bbd5375cf39d193367b61b418`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c212d22018c8ed56b082699241fba4b6a975dcc80941663d3333e79726ef710`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120f89b8213b7712056cc20c3454b43dfbefee8092827722ba2bd7183f6693ea`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.7 MB (22744744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbe59c92ae308cc1ca95460830da582ea729bd502e6fdcc9e91a0980a0cf7f0`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24199190c27c55807d7aa76cacb9f25e09fbcbaf0385f92d8088eed73e875917`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f962b02a3d44056e12be508848bc41eb716d98ca72374c1e979fbcd1cf7c7`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ac0a28f0cff7f101228c34c93dbaf640a640f1ee5472053393f4931082d129`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.3 MB (22281907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:c780cf7ac1c5c0cb9599b2df0349dc29186be36aae111d30e399c208f227ae72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:8b2723933f4e20b03d82fad4f272979c45d21e29d5d5437a257dddd7a19b69e9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216826173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad7864511de6cf197875bc99d7c27cee1e5e4a9511cdb529bf075ad6e87eed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 18 Mar 2025 17:52:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:53:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:53:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:53:59 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:54:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:54:10 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:54:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efae6d46cdd88fc96e587336604ae353dae631d3edfb17299749b56f042f86e`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabff009c2b284cea2d40695c1b44d8b2e2b9a499dca58e92884fc4c4139d19b`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 338.8 KB (338767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299a5346171e96e11bbf7e75d2c923c9e767db919ae268e6303f0a8b51505132`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5681385a5fb68fbaf1d531ba43ef1a4eebca86ff9357c638c2b7ab8722096c`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bf621533bae634d522d1baa809d4030a69957056c545455ed8a6b54a582f37`  
		Last Modified: Tue, 18 Mar 2025 17:54:28 GMT  
		Size: 19.8 MB (19814343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d74b41781047bb821590370c205f708cb1312ac611cf3ffa7d92817cb3385`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8fd088b8dce22bb00a6dae4b3c11ff824bc93bbd5375cf39d193367b61b418`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c212d22018c8ed56b082699241fba4b6a975dcc80941663d3333e79726ef710`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120f89b8213b7712056cc20c3454b43dfbefee8092827722ba2bd7183f6693ea`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.7 MB (22744744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbe59c92ae308cc1ca95460830da582ea729bd502e6fdcc9e91a0980a0cf7f0`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24199190c27c55807d7aa76cacb9f25e09fbcbaf0385f92d8088eed73e875917`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f962b02a3d44056e12be508848bc41eb716d98ca72374c1e979fbcd1cf7c7`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ac0a28f0cff7f101228c34c93dbaf640a640f1ee5472053393f4931082d129`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.3 MB (22281907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:1602a0714e35d9428df55b3574afa737262d7899f2981edad083d6958065b422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:83ff96ddbee1bd02aa91285b3bf9690d98b899aff79585b714f4db4fa5fffcc7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335201497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a81d38ebdc303a8a3364a74efe23a1bedf44c1d7b8e6eed9a8be08f2556ec27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 18 Mar 2025 17:48:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:18 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:48:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:48:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:28 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:48:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:48:30 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:48:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:48:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:48:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:48:41 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:48:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f078092de8abb6d57d53e680c3076c9ef2bfbbf71c6f4a21348b227be48e4`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf4f863fc1275088515214a01de99ac68d3bfe956ba35597d3baa916414bfc7`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 364.5 KB (364474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6be91d2a668f124038a4b58fd4ea66112de7b5b0b97a139693dfad7af569f`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2113532490862d3f6fbbc444054df6a45ac27fd7df836514bba886616282d1e`  
		Last Modified: Tue, 18 Mar 2025 17:48:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed759800fa7e1df988ee6bd77b70fb0ff86c479116b939808e48316290b16876`  
		Last Modified: Tue, 18 Mar 2025 17:49:00 GMT  
		Size: 19.8 MB (19826177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8359603b2119f0fa8a6571abae59b6fedadab69d593491f5654da2369da6101`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8691616fbb1ac24ed70ed40459202a0890dc879db4b4bd145bf682fe91a5f35d`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fede937bf0332135d9e85cd74b71cdabff018cd49fdb00377c1c8b6a955a98`  
		Last Modified: Tue, 18 Mar 2025 17:48:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df182fa0d8efc357ce076453fa75808da26e64d896888a663012d878865f2516`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.8 MB (22756719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662cc6465c91f282c1f13da905ddbb3283da516701570a3ba3bbee34f45732ee`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ce90bd08504a907b943a9371e9bc6cee33b2bfce11817ab311fde6581cf9a6`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afc5eb0fd1f12683a0f679fa6e3e6ec671d4c5216693af8d75aae719eb8775f`  
		Last Modified: Tue, 18 Mar 2025 17:48:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab8c7824ed6e25645587020a647c04eb9024db067d572ea1afed4d07eb063a`  
		Last Modified: Tue, 18 Mar 2025 17:48:57 GMT  
		Size: 22.3 MB (22301399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:4c2d528f844dac99062dc79967dd48348177d2db9ea7c66e86dd29010b571301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:81996f945dd6afd17a2f454f627cc9301a6d669d579eee88075c6866592b7eac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974045827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90411219e91a7a2282d6bafa1fa9f88374b9cc7fc5023a00346072afe20d252f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 18 Mar 2025 17:48:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:59 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:49:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:49:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:13 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:49:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:49:15 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:49:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:49:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:49:28 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:49:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0cd020c6471f62220ad8ed2ae2b3772b806f467cb0f11bc4308b9f2d0d26a`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cf4955d1aad1f83447efbdbcf08c9bd7423c84e7c6ac5bc6a5625140c991e0`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 400.2 KB (400166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90786f2c40deca413eed711fbbeb0abe197cababcf2e8b187fda5466bf3f9e14`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684238c758b95728bef5bbcf3815bce65fcb21040c3ec400e17b2e4b2975988`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7eac4b401484a405d9d595d4ab1ab2e2fa8f1dc11da64e453e0d575e376817`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 19.9 MB (19862606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68379e676f653db1ef6496f93f7f34f94e2e6adc3897f119f4d93a2092313f0`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df3c74807df3393363f62fd1b3dec83fe3a43f74559b92815cd5cbd580fbe6f`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5332d7c8bb3be4f3f08437752f48d8a66371aad10f5328510eeaa532db9383ba`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebe5ad6be9c69cb89a53b45d42605e0654403950049245df6ed82d6552beb2`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.8 MB (22789480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7945eb3de2b551bb141ecdcf88f5508c82ba67aa0f4910a08e9833a279946fde`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32749cc1ae150ad64cd11025c4de890ad6f72d84ccb8714200245b156bf136d1`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598bafa4dd3f7f04b9861f17341c80a693efdf2c84a11ab664533e4b3c2334b2`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b541b6491c1b4a89b6665a2775f4c706b4f2d8349747d04f83ac14f4ac23ca`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.3 MB (22334051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
