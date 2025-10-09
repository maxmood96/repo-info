<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.5`](#docker285)
-	[`docker:28.5-cli`](#docker285-cli)
-	[`docker:28.5-dind`](#docker285-dind)
-	[`docker:28.5-dind-rootless`](#docker285-dind-rootless)
-	[`docker:28.5-windowsservercore`](#docker285-windowsservercore)
-	[`docker:28.5-windowsservercore-ltsc2022`](#docker285-windowsservercore-ltsc2022)
-	[`docker:28.5-windowsservercore-ltsc2025`](#docker285-windowsservercore-ltsc2025)
-	[`docker:28.5.1`](#docker2851)
-	[`docker:28.5.1-alpine3.22`](#docker2851-alpine322)
-	[`docker:28.5.1-cli`](#docker2851-cli)
-	[`docker:28.5.1-cli-alpine3.22`](#docker2851-cli-alpine322)
-	[`docker:28.5.1-dind`](#docker2851-dind)
-	[`docker:28.5.1-dind-alpine3.22`](#docker2851-dind-alpine322)
-	[`docker:28.5.1-dind-rootless`](#docker2851-dind-rootless)
-	[`docker:28.5.1-windowsservercore`](#docker2851-windowsservercore)
-	[`docker:28.5.1-windowsservercore-ltsc2022`](#docker2851-windowsservercore-ltsc2022)
-	[`docker:28.5.1-windowsservercore-ltsc2025`](#docker2851-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:7c3953162b1feca2aeb68a88ccb206485ff8c06177352ed9ffb3606354837869
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
$ docker pull docker@sha256:17dd9c4154d3ca889b5b31e3e4b2818645819996f456e6c3e17b581737a44640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148653816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6219f96c48a526ca01fa59e2eca65ec67cd3f979f6c48dedeb14e6697dc42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0774022190f2b752e87a84c66b9a6ff1b3bbae43c893a860bd9a3fcbc4290ca`  
		Last Modified: Wed, 08 Oct 2025 20:34:07 GMT  
		Size: 9.5 MB (9507816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a691ee9764b4b3f4d9affb8c29ffc03f4c4d989298e2b2bfb93f4331b46f7`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a961a73cdd2322e8f59b2d11b5b5f03c41e6e488e12cb58d8a99bd02721ba90`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eaed86521d704b815068678197393163d0e1dc0dacde55392442b31b2bd192`  
		Last Modified: Wed, 08 Oct 2025 20:34:13 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49f61d997913f33514036426a2065cebcfafe63fa9d6464806bab8cff14914`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4b3e1409309a4af29d18da4edc4d1e06493028905509bce28eab52f2830e2`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:83e9d11602839d96665359ff81acf502ca43128754c722e7e02d5485220c97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ebaedf942d951b446ca1d48457cc7c468773b27f124b9f82e2761ec02af24`

```dockerfile
```

-	Layers:
	-	`sha256:60b958c4eb2101a33fd57b379ecb3eaddf7b960fa6558ae1e09fc807a11af41b`  
		Last Modified: Wed, 08 Oct 2025 23:07:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:23a94b59cfc54fb3f0a85562f77e1976ae427b6702eda1a6cc05665877ea7b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139351050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ad2dd9699bda1ab2c7d47dae8a76a2b693177a5f21a4d6ce52b8b5d54dc3f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7287652ad0f7417ae457a402f40a248670eddecae812df05328d7506b4eb7e`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 8.1 MB (8113337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431c8dbca316340be018038caec6bbb46de520002d7da495df2f3e22849718e`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2563734e87d4a41e756c5736d441c0d579cf5894976488bda29c158ca7b63c`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 18.4 MB (18418117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a98f22f147edc4650160e65326ae9aba04a825e888134bed99a30de9924eec`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e91a5ae2992f9361c096f7b969cbecfda20fe4c12e9c334d78dd56773286d8`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.4 MB (20371581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a13a1e08f9cd1e0584b24d8da93cf0b6f5047eeaf877caab0f4e47c1995081`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ecb3b6457a07ed0380f10034b6b0c3debcedce2a293f27f758b11cea20773f`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfb0083d4b0f462cdd77af85a4fc4fa2a17d49e30ec95f875998c1f8e27c759`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f97c4423935104b21120f03a4a4115af7e34c6549f33ba3f728f62acd6d3f8`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 9.5 MB (9461590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f59d52b9ff498c398252d10538d93ccda3c0928772008c1888f81cb9d58194f`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 90.0 KB (89976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555d288334111b4ea28df2e84d6e78b4a9351fef638dc5b83b1627892ede34c`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de61bedb5fac1b2191c9f3ab0f3dffca84f002acff72b937d528ff96cbf4d14`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.6 MB (58629069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e881d9a90366a6825183c33b18cb2464e9c0ba0ecb7195e91e15ab09201a7`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a5c01ee4ee6468b4679313e14ac47b9ae9211a3a82b2c619a88f3d050eda0a`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:6e1b8fdc4984c0332556dbbf675047c01e0dc730a44ba6a1d254bc3bfb80e104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486c5363be4c09b70896b0b3db97db56de5f1226ca63de5ab425ff9453c4e46`

```dockerfile
```

-	Layers:
	-	`sha256:788a52ad55210bd2d4ed9fbbd6a152ba7b14dc3b7ee4c53d0f3a5cdedddf22d2`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:556db6b0e9df61bc612f019a8d4f6b5893969e89ddef9a58ffda03de01db0986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137322880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80105514d7c10daa8dcca6c73d62d0fcfcff8aef05f53027ed8f5b1e79221ea2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cbf04f008d9ef02dc799e294f7dfb15a6e1a7aa998c3ebd1abf85624fd8a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 7.4 MB (7437673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1a1cead3e82bc31db9d8227c36601c068da1b29538ac729dc38b62a255fa5`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73fe5fd8d6e91b61f554e5f4b6b205576d456d3ff11c7c7ae9f52c5dcbcb470`  
		Last Modified: Wed, 08 Oct 2025 20:23:28 GMT  
		Size: 18.4 MB (18402565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903fc967e46d7ed98ec9852c40659425d0fb55abfe4f3114b15a6d051a4c554f`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd58177b493833da3bb70027bbd00cd33ec2a6a6b37a4d8902ac62484e484b`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.4 MB (20352523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bada26e2a877a929758e22c849d20f156052c10b2613fc9122bf7b4e0d47050`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1b317dd5ec27fce62f574f1407e0d4893a1fe837e0e400de6dad22af04a1a`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35505dbf43402553e3b3c3b3c5f96a72c4772064bb797056463d77c9ced603d6`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cdb6aaff8e793882f2f2c50f51ed0c543232f7ab61ec1a55f57a7fff20e9fd`  
		Last Modified: Wed, 08 Oct 2025 20:54:16 GMT  
		Size: 8.6 MB (8610534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565524eb45b33cca7682947b28d97afa084eef35709cac083c7154e7ee93cb0`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 86.4 KB (86414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9137482da6d642b27169cbfe86fc0512df0e52ca658835c1e4a3354f9bdc05`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8654f9a663a2d9b3e893f06fd452e75bae44e486b46bd0acbf041c75356cfc5`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.5 MB (58461578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882f3a2fa1333d7ac2956f36df7b2ef37b65a14f4cd5a4a740b0bd54d1984e4`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509993fdecc5bd3d307dd22ffb54af7aebf642e0155a25d6035c07102dd71f5`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:2d13d67ca9ef63f5eae6bba37fa287fcd66f661a5ab7002efbc8cb272edf5e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49ceb1c2519c405e3dfb782a06e6b1843eafc37059e91f61f0dfb01d8e828b`

```dockerfile
```

-	Layers:
	-	`sha256:843f07fbd7ee6fd55be49dd57f9c2124b4545c2bfe2d8430d990874abce54d87`  
		Last Modified: Wed, 08 Oct 2025 23:07:39 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9449b06cd22f308c6da3438072219d67a8f97108a97592e085569dae2ccdfc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139518141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fb75ea8a70cd3e982f7092098519a9358044c47278398e2b0e6584159ff182`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb8af46f57d19a7eff37ee20d0f745f2b25c2db3b03f886c5a262a2f978a5e`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 8.2 MB (8227626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e992b003cff6ac506b5770b58db53b0f264a7863c746e93a526eda5371cbb67`  
		Last Modified: Wed, 08 Oct 2025 20:25:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad120ba60793ead7541cf11a93928a23a8096c556b455d71e627b4770101eaf`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.2 MB (19232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bffd5eefa70b71759fe0ba576c4e5a833cd108f5798c6b7a09fe803268b02a`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e293265a4a953b06a80ea42dcf65f5105661e35dcd4e3db9929129fcbaef9`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec633ce7cb5252722f81f70be756b95d7ece1d440cd03c2b8e47cc8e81c6f3`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebf8988ea011982152e9840872446a584f00fba937e96bcbeb387ad10c2aca`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34003f92833935910091b03a75c728b9d21498e4db1400fd148a1efe0657544b`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f803108a8d61186171f4e10fe37dc2d290ac0b06ea7697d287f65327d18754fe`  
		Last Modified: Wed, 08 Oct 2025 20:33:22 GMT  
		Size: 10.0 MB (10032583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf713f8b6955fe83fa08d31cd4c30540fd734f00883ec9c827b12637f1baddd`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 99.5 KB (99542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9df8ad4f1ac1a4a2e84cf23938b4fc4a9d2aa2cdf2f3a0ef3611e36bb5f90c`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe98abb3a4ed4d7df089ae860cee02629c5ad7d91820952b15b2965d109ee2`  
		Last Modified: Wed, 08 Oct 2025 20:33:26 GMT  
		Size: 57.8 MB (57758061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241f05e886b9dc02131bb575c75a464cd577a7a7e082f41993e2180d95dc367`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fff9ec4efe80e48bed7b9607d6734de8054195e33b010de9d037f452d0a03d`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 3.3 KB (3292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:b8efda5d1a7b765ec59ee503923e04d468f4202d8e4bd77ad5acc8ece82bfa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691659727245be56f7f4184be548de4c6f5841acc17ac30efe2d295503f06208`

```dockerfile
```

-	Layers:
	-	`sha256:1ea5e87c40e396c7f276887066b70aa11aa4cfabe79495c6ab35d902bb65a04b`  
		Last Modified: Wed, 08 Oct 2025 23:07:42 GMT  
		Size: 34.8 KB (34831 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:19b6a32c14b2d71c0ef4575f6ad1712dca6f23f73155a60bb07c0d1f4fb00418
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
$ docker pull docker@sha256:2ceaba2d9fe94568625978458a4f93e81b294fb96927fe2602b2cedd0bf9aea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76218700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6fa733b2ab715cbe441dd3c8359166d4973a32bd0dd734ee6ae29d4674c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f0a7b75fac3ac0bdc9c259b3dee99d1b76ee443dac8cfba8dd29f35c802a2c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faabc0adf6d1af8f9982e75c4aa3764cfb09e6b1e25ea0d359271125a065cdf`

```dockerfile
```

-	Layers:
	-	`sha256:c9a093a89c86df61de202e883b8edc52d7bda13f8a30db29a33e6bb0cd17fb1e`  
		Last Modified: Wed, 08 Oct 2025 23:07:49 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ee987cd4ffdfcf157a4df2756fe649bcf28040e3120405621f2106d5b95a65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71167610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8797fa6025da5f6cf43e5c7d5a861a13c1310981b47c73deaf111403fc763d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:913a776a1640e30a4787299519798eece3065c0a11f093478d4fd2729f8d09f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb92b7516dfaf1ff47deaa4c43d8c5da5e5d5a3063009bcbfaca11b0f4638e`

```dockerfile
```

-	Layers:
	-	`sha256:c6429b41ec7e43b858d6fc47cfbdf63b75084dd78f7a456a4109e8ef5fa7d9ae`  
		Last Modified: Wed, 08 Oct 2025 23:07:52 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ca49543195a1e53642ae43f301269504f6157911c85df2e1fe9a48f2b641a5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70160704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3864f57cedbc27d92173d6ce1ff98bd62deb24f2f012baa9bfd8c86bd18a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:27cfbd43240b2a36d9206e8d65ffa68cc828cc333dee94860ea8fe50fcdedc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54f87f9a325c1a28f3911b733bb8d436d5a344e5f4cab025423060c3122f12`

```dockerfile
```

-	Layers:
	-	`sha256:1c73b917de5769ed1585050836dd77eb606db44134e96525d7b6be3ce44aa0d5`  
		Last Modified: Wed, 08 Oct 2025 23:07:56 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a246a4a6c87424fc8e26fbd5f8f26e1ac19e2745da7e3c40be18b8c265ae1bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71629206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9625f7aa2680d221b2ee306d6dd46be38d361c45cde6e47d84115ebc8faa619c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b2a82343ac247cca758d9a1cf13ec29c7705a3d4f11eac33840976a005f375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcf6dab5064a1fd34f33a9e7a5856d82a8f5ae4eb063493a494c9439eda61ad`

```dockerfile
```

-	Layers:
	-	`sha256:7879f0a2aa84744862fb9b29e3a5a4bcf9495ec25822e20b5e68e59056b15992`  
		Last Modified: Wed, 08 Oct 2025 23:07:59 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:7c3953162b1feca2aeb68a88ccb206485ff8c06177352ed9ffb3606354837869
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
$ docker pull docker@sha256:17dd9c4154d3ca889b5b31e3e4b2818645819996f456e6c3e17b581737a44640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148653816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6219f96c48a526ca01fa59e2eca65ec67cd3f979f6c48dedeb14e6697dc42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0774022190f2b752e87a84c66b9a6ff1b3bbae43c893a860bd9a3fcbc4290ca`  
		Last Modified: Wed, 08 Oct 2025 20:34:07 GMT  
		Size: 9.5 MB (9507816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a691ee9764b4b3f4d9affb8c29ffc03f4c4d989298e2b2bfb93f4331b46f7`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a961a73cdd2322e8f59b2d11b5b5f03c41e6e488e12cb58d8a99bd02721ba90`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eaed86521d704b815068678197393163d0e1dc0dacde55392442b31b2bd192`  
		Last Modified: Wed, 08 Oct 2025 20:34:13 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49f61d997913f33514036426a2065cebcfafe63fa9d6464806bab8cff14914`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4b3e1409309a4af29d18da4edc4d1e06493028905509bce28eab52f2830e2`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:83e9d11602839d96665359ff81acf502ca43128754c722e7e02d5485220c97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ebaedf942d951b446ca1d48457cc7c468773b27f124b9f82e2761ec02af24`

```dockerfile
```

-	Layers:
	-	`sha256:60b958c4eb2101a33fd57b379ecb3eaddf7b960fa6558ae1e09fc807a11af41b`  
		Last Modified: Wed, 08 Oct 2025 23:07:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:23a94b59cfc54fb3f0a85562f77e1976ae427b6702eda1a6cc05665877ea7b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139351050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ad2dd9699bda1ab2c7d47dae8a76a2b693177a5f21a4d6ce52b8b5d54dc3f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7287652ad0f7417ae457a402f40a248670eddecae812df05328d7506b4eb7e`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 8.1 MB (8113337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431c8dbca316340be018038caec6bbb46de520002d7da495df2f3e22849718e`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2563734e87d4a41e756c5736d441c0d579cf5894976488bda29c158ca7b63c`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 18.4 MB (18418117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a98f22f147edc4650160e65326ae9aba04a825e888134bed99a30de9924eec`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e91a5ae2992f9361c096f7b969cbecfda20fe4c12e9c334d78dd56773286d8`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.4 MB (20371581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a13a1e08f9cd1e0584b24d8da93cf0b6f5047eeaf877caab0f4e47c1995081`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ecb3b6457a07ed0380f10034b6b0c3debcedce2a293f27f758b11cea20773f`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfb0083d4b0f462cdd77af85a4fc4fa2a17d49e30ec95f875998c1f8e27c759`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f97c4423935104b21120f03a4a4115af7e34c6549f33ba3f728f62acd6d3f8`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 9.5 MB (9461590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f59d52b9ff498c398252d10538d93ccda3c0928772008c1888f81cb9d58194f`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 90.0 KB (89976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555d288334111b4ea28df2e84d6e78b4a9351fef638dc5b83b1627892ede34c`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de61bedb5fac1b2191c9f3ab0f3dffca84f002acff72b937d528ff96cbf4d14`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.6 MB (58629069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e881d9a90366a6825183c33b18cb2464e9c0ba0ecb7195e91e15ab09201a7`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a5c01ee4ee6468b4679313e14ac47b9ae9211a3a82b2c619a88f3d050eda0a`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6e1b8fdc4984c0332556dbbf675047c01e0dc730a44ba6a1d254bc3bfb80e104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486c5363be4c09b70896b0b3db97db56de5f1226ca63de5ab425ff9453c4e46`

```dockerfile
```

-	Layers:
	-	`sha256:788a52ad55210bd2d4ed9fbbd6a152ba7b14dc3b7ee4c53d0f3a5cdedddf22d2`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:556db6b0e9df61bc612f019a8d4f6b5893969e89ddef9a58ffda03de01db0986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137322880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80105514d7c10daa8dcca6c73d62d0fcfcff8aef05f53027ed8f5b1e79221ea2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cbf04f008d9ef02dc799e294f7dfb15a6e1a7aa998c3ebd1abf85624fd8a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 7.4 MB (7437673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1a1cead3e82bc31db9d8227c36601c068da1b29538ac729dc38b62a255fa5`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73fe5fd8d6e91b61f554e5f4b6b205576d456d3ff11c7c7ae9f52c5dcbcb470`  
		Last Modified: Wed, 08 Oct 2025 20:23:28 GMT  
		Size: 18.4 MB (18402565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903fc967e46d7ed98ec9852c40659425d0fb55abfe4f3114b15a6d051a4c554f`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd58177b493833da3bb70027bbd00cd33ec2a6a6b37a4d8902ac62484e484b`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.4 MB (20352523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bada26e2a877a929758e22c849d20f156052c10b2613fc9122bf7b4e0d47050`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1b317dd5ec27fce62f574f1407e0d4893a1fe837e0e400de6dad22af04a1a`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35505dbf43402553e3b3c3b3c5f96a72c4772064bb797056463d77c9ced603d6`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cdb6aaff8e793882f2f2c50f51ed0c543232f7ab61ec1a55f57a7fff20e9fd`  
		Last Modified: Wed, 08 Oct 2025 20:54:16 GMT  
		Size: 8.6 MB (8610534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565524eb45b33cca7682947b28d97afa084eef35709cac083c7154e7ee93cb0`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 86.4 KB (86414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9137482da6d642b27169cbfe86fc0512df0e52ca658835c1e4a3354f9bdc05`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8654f9a663a2d9b3e893f06fd452e75bae44e486b46bd0acbf041c75356cfc5`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.5 MB (58461578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882f3a2fa1333d7ac2956f36df7b2ef37b65a14f4cd5a4a740b0bd54d1984e4`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509993fdecc5bd3d307dd22ffb54af7aebf642e0155a25d6035c07102dd71f5`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2d13d67ca9ef63f5eae6bba37fa287fcd66f661a5ab7002efbc8cb272edf5e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49ceb1c2519c405e3dfb782a06e6b1843eafc37059e91f61f0dfb01d8e828b`

```dockerfile
```

-	Layers:
	-	`sha256:843f07fbd7ee6fd55be49dd57f9c2124b4545c2bfe2d8430d990874abce54d87`  
		Last Modified: Wed, 08 Oct 2025 23:07:39 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9449b06cd22f308c6da3438072219d67a8f97108a97592e085569dae2ccdfc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139518141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fb75ea8a70cd3e982f7092098519a9358044c47278398e2b0e6584159ff182`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb8af46f57d19a7eff37ee20d0f745f2b25c2db3b03f886c5a262a2f978a5e`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 8.2 MB (8227626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e992b003cff6ac506b5770b58db53b0f264a7863c746e93a526eda5371cbb67`  
		Last Modified: Wed, 08 Oct 2025 20:25:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad120ba60793ead7541cf11a93928a23a8096c556b455d71e627b4770101eaf`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.2 MB (19232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bffd5eefa70b71759fe0ba576c4e5a833cd108f5798c6b7a09fe803268b02a`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e293265a4a953b06a80ea42dcf65f5105661e35dcd4e3db9929129fcbaef9`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec633ce7cb5252722f81f70be756b95d7ece1d440cd03c2b8e47cc8e81c6f3`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebf8988ea011982152e9840872446a584f00fba937e96bcbeb387ad10c2aca`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34003f92833935910091b03a75c728b9d21498e4db1400fd148a1efe0657544b`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f803108a8d61186171f4e10fe37dc2d290ac0b06ea7697d287f65327d18754fe`  
		Last Modified: Wed, 08 Oct 2025 20:33:22 GMT  
		Size: 10.0 MB (10032583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf713f8b6955fe83fa08d31cd4c30540fd734f00883ec9c827b12637f1baddd`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 99.5 KB (99542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9df8ad4f1ac1a4a2e84cf23938b4fc4a9d2aa2cdf2f3a0ef3611e36bb5f90c`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe98abb3a4ed4d7df089ae860cee02629c5ad7d91820952b15b2965d109ee2`  
		Last Modified: Wed, 08 Oct 2025 20:33:26 GMT  
		Size: 57.8 MB (57758061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241f05e886b9dc02131bb575c75a464cd577a7a7e082f41993e2180d95dc367`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fff9ec4efe80e48bed7b9607d6734de8054195e33b010de9d037f452d0a03d`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 3.3 KB (3292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b8efda5d1a7b765ec59ee503923e04d468f4202d8e4bd77ad5acc8ece82bfa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691659727245be56f7f4184be548de4c6f5841acc17ac30efe2d295503f06208`

```dockerfile
```

-	Layers:
	-	`sha256:1ea5e87c40e396c7f276887066b70aa11aa4cfabe79495c6ab35d902bb65a04b`  
		Last Modified: Wed, 08 Oct 2025 23:07:42 GMT  
		Size: 34.8 KB (34831 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:eeb43ad630a5165c910f03041a590147ddb1c2632be3a3c397e9b2c2b4efa7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:b3d53c924e34d7e003f601d8d6222844b9c1b71b7aa0b2ed4655a6b30fe32602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169675916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78479fdc55be9d0c2772a94ab8b66e905f686b58a754da0f12cd11b4ba460167`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD []
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f4121261305cd808f866e5cc468c62c7b691048458ce84c73cebc8744a0f5c`  
		Last Modified: Fri, 03 Oct 2025 15:42:57 GMT  
		Size: 8.2 MB (8206013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacb763c34fa98faf157ad30ac845055c7e17d6bc356a735dd34979b2ca3dcd`  
		Last Modified: Fri, 03 Oct 2025 15:42:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82baaa61b0bd5e833b9bf0dce2a5ba042e651d1dae98dcecd76a54d85245f705`  
		Last Modified: Fri, 03 Oct 2025 15:43:00 GMT  
		Size: 20.4 MB (20429721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c233148e55acfe21ab7559acf33645c62cab15c2786fb755b117d0f761692214`  
		Last Modified: Fri, 03 Oct 2025 15:43:04 GMT  
		Size: 22.2 MB (22158310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a01365128829f855670516e240e079aaa07cca78da2106a03fe8cc88723c3c6`  
		Last Modified: Fri, 03 Oct 2025 15:43:10 GMT  
		Size: 21.7 MB (21656766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d97b7b769f0ef0ffff5fb8721b8852aab640d625cccad858457c7ccdc01909`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252ca38c80c99c59f88eb9177337a5d1e1be51a71bca74077ce10d0e2db2ff6`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f710bb1cc914e30eac705c8d79e2b6fac559197d538c0a843bfdd992a69bfe1`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bd32a0ea96da36ee694f909a448f72d9ce8f3161366150204ce43f92f3ef25`  
		Last Modified: Fri, 03 Oct 2025 16:55:35 GMT  
		Size: 9.5 MB (9507812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b78db0b14600437995bb4b41a16d542cc1c29e47d131a154fcd0e71e1240e7`  
		Last Modified: Fri, 03 Oct 2025 16:33:46 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02844b1b965c7106b174fa8fcc81da5932ae550f52b2cdea2f4b1cbc72cf9103`  
		Last Modified: Fri, 03 Oct 2025 16:33:51 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c0d4f3fc3deda7540f99bf89eb4616d8fe2bf6fde04101d3c62817b55b32ed`  
		Last Modified: Fri, 03 Oct 2025 16:55:36 GMT  
		Size: 62.8 MB (62827332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2b4197469badf8d75becb38e327e689d7b466f9a06cbf2e22c1574489684fc`  
		Last Modified: Fri, 03 Oct 2025 16:33:54 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733f9fcc3eeee9d72d8b472b1225e3228f39f1cefe71d8dff9f1a2c710decce`  
		Last Modified: Fri, 03 Oct 2025 16:33:57 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac14d1bbef2a00ee6148a84da6d122959f4469478e896e6b0238d37228c12e58`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 3.4 MB (3398331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a4cba6aa490126672884ec1cc7fc81c87c39f7a7b752a3a27031de81cc7e66`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3068b13530be21c371198cff4b2617ff2f7bf794a5ff5f9daf01addd778aa4b0`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aed80e8577ba3b89d9e8425fc00a705532e626ca3fc051bad538409c0399762`  
		Last Modified: Fri, 03 Oct 2025 16:56:14 GMT  
		Size: 17.6 MB (17592032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069ff56a1905eb0680d22ee4587a1a1ba638f709814aca49b750b3c4bf3531f6`  
		Last Modified: Fri, 03 Oct 2025 16:56:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:93a89793da5adcc19ef3c9827d45c6ecb2767c1a1585dc874a34e2e3565f084f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119379607dbb4d2e6842aa149d585b6259e03e4b136a8b29a877d1fd94e7a05f`

```dockerfile
```

-	Layers:
	-	`sha256:91562a8e6c08e44f1300395f13fbf8c2f9e8521ccc3a5a2685e8553f477b409e`  
		Last Modified: Fri, 03 Oct 2025 17:07:59 GMT  
		Size: 30.6 KB (30636 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:96a3c2358a11eb6c0b8b8697af03c763b040a4289d5cdb41afce7cccfdc6a7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160960944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09fc28f780b87f424eac4f8d8e1a3e2f8b076509e298aa9f1c3af3ce13c6945`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD []
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befee8c2b0ad40f8afec285692dd9de306244ab77849362b32f364598f4dd856`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 8.2 MB (8227655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81db965703fb492a9487f0707728f846ca5016cffbe4cca14a9aaedf3fe47be`  
		Last Modified: Fri, 03 Oct 2025 16:10:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae023da43925318e9d906c7752c90968e4e76401eff1a13c13a02dfad260775`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 19.2 MB (19238158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d084ed095dcaaa56e75d1464d58172ca160961091fd6c2110b81301c1c8d144a`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 20.3 MB (20274240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5cbf3334db63fb72ebb37340a3158221d6151607e4b01c5be6b44f4c2a1f35`  
		Last Modified: Fri, 03 Oct 2025 16:10:10 GMT  
		Size: 19.8 MB (19779981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a37c322750556c7e8922a42c05e513ce640dbe5059b406843b4285c15f28be`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ee98d68b79d3a825b7c3d7d4492c505cae7e7ee829b8da41259b5372f704be`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06880fc24b1d74868cf537077a0bd0cc09b9cb315d6f2e5ba9ae3fe57405085f`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e663db0fdfaf3e5f40f7c3d7c3d51cfa62bbe43ddfcb4fe99cb8b6c637f6aa`  
		Last Modified: Fri, 03 Oct 2025 16:11:02 GMT  
		Size: 10.0 MB (10032639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5e31e2508033fa71a6e9c996b28c63fb8717b1fb04950cc9bf8ab9c496715c`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 99.6 KB (99551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44d97f98752505c225f3d7bf9a163d9522bb8c15f839dde10ca592bec612151`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db3a1adaf72d283f41dd82a794dd8a21401cf97b9547986d552142a747eb5ae`  
		Last Modified: Fri, 03 Oct 2025 16:11:06 GMT  
		Size: 57.8 MB (57759208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0ea7e65ba6a9a348e2c362f6ee2128c9cbbc4fe766157fac25a52324ef2e0c`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8003cd90da085be86d46c270b3ffed416d670d6fb46dc211845eaad27c21794`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210fc14d10dd6889f85a6c0dda51131547e11a4b09c342a41f267e3b05025bb`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 3.4 MB (3389873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650ea26cdb1e4676d6bce162d7e5a937b93e2705cc86380b54dd03d1e8b1abd3`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5728e12ff2b23e1c18b5c20970862362841a7011baa80aef4a45d5a1b108115`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30951d5b864c3c60fe2adf5433ff9e1d915fc52fdd40fae1766a1948ac8ef345`  
		Last Modified: Fri, 03 Oct 2025 17:08:19 GMT  
		Size: 18.0 MB (18019399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056d88955c46abf8014f4e3163803203a97c96513ab2783aee987fd1cc078700`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4025f450b00c6226d6682f17fbdaa8ff0aca575e36b82377be3680a70b1008ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd180d64e35b20ae847a8335cd5554d37b68ed547c4530d96e617dd92f1a9a0`

```dockerfile
```

-	Layers:
	-	`sha256:e94643b935420367d72f27be406ef5a64f8862ab497d1cb7c6291454821ec49c`  
		Last Modified: Fri, 03 Oct 2025 17:08:03 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:337c819e1e92bbe665964fa9ff8420a91cd889d8b99ba336749af5eb20bd5502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:08fcf22b324f01b24d7d6c9edb2a077743fcb7a420e4263f0b1bca4952e41c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a850d0d3454900418bf8bd97acb002622a6ed5b1a77fa6fd76412b1f4f8ef768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5`

```console
$ docker pull docker@sha256:7c3953162b1feca2aeb68a88ccb206485ff8c06177352ed9ffb3606354837869
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

### `docker:28.5` - linux; amd64

```console
$ docker pull docker@sha256:17dd9c4154d3ca889b5b31e3e4b2818645819996f456e6c3e17b581737a44640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148653816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6219f96c48a526ca01fa59e2eca65ec67cd3f979f6c48dedeb14e6697dc42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0774022190f2b752e87a84c66b9a6ff1b3bbae43c893a860bd9a3fcbc4290ca`  
		Last Modified: Wed, 08 Oct 2025 20:34:07 GMT  
		Size: 9.5 MB (9507816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a691ee9764b4b3f4d9affb8c29ffc03f4c4d989298e2b2bfb93f4331b46f7`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a961a73cdd2322e8f59b2d11b5b5f03c41e6e488e12cb58d8a99bd02721ba90`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eaed86521d704b815068678197393163d0e1dc0dacde55392442b31b2bd192`  
		Last Modified: Wed, 08 Oct 2025 20:34:13 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49f61d997913f33514036426a2065cebcfafe63fa9d6464806bab8cff14914`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4b3e1409309a4af29d18da4edc4d1e06493028905509bce28eab52f2830e2`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5` - unknown; unknown

```console
$ docker pull docker@sha256:83e9d11602839d96665359ff81acf502ca43128754c722e7e02d5485220c97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ebaedf942d951b446ca1d48457cc7c468773b27f124b9f82e2761ec02af24`

```dockerfile
```

-	Layers:
	-	`sha256:60b958c4eb2101a33fd57b379ecb3eaddf7b960fa6558ae1e09fc807a11af41b`  
		Last Modified: Wed, 08 Oct 2025 23:07:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5` - linux; arm variant v6

```console
$ docker pull docker@sha256:23a94b59cfc54fb3f0a85562f77e1976ae427b6702eda1a6cc05665877ea7b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139351050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ad2dd9699bda1ab2c7d47dae8a76a2b693177a5f21a4d6ce52b8b5d54dc3f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7287652ad0f7417ae457a402f40a248670eddecae812df05328d7506b4eb7e`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 8.1 MB (8113337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431c8dbca316340be018038caec6bbb46de520002d7da495df2f3e22849718e`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2563734e87d4a41e756c5736d441c0d579cf5894976488bda29c158ca7b63c`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 18.4 MB (18418117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a98f22f147edc4650160e65326ae9aba04a825e888134bed99a30de9924eec`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e91a5ae2992f9361c096f7b969cbecfda20fe4c12e9c334d78dd56773286d8`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.4 MB (20371581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a13a1e08f9cd1e0584b24d8da93cf0b6f5047eeaf877caab0f4e47c1995081`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ecb3b6457a07ed0380f10034b6b0c3debcedce2a293f27f758b11cea20773f`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfb0083d4b0f462cdd77af85a4fc4fa2a17d49e30ec95f875998c1f8e27c759`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f97c4423935104b21120f03a4a4115af7e34c6549f33ba3f728f62acd6d3f8`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 9.5 MB (9461590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f59d52b9ff498c398252d10538d93ccda3c0928772008c1888f81cb9d58194f`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 90.0 KB (89976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555d288334111b4ea28df2e84d6e78b4a9351fef638dc5b83b1627892ede34c`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de61bedb5fac1b2191c9f3ab0f3dffca84f002acff72b937d528ff96cbf4d14`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.6 MB (58629069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e881d9a90366a6825183c33b18cb2464e9c0ba0ecb7195e91e15ab09201a7`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a5c01ee4ee6468b4679313e14ac47b9ae9211a3a82b2c619a88f3d050eda0a`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5` - unknown; unknown

```console
$ docker pull docker@sha256:6e1b8fdc4984c0332556dbbf675047c01e0dc730a44ba6a1d254bc3bfb80e104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486c5363be4c09b70896b0b3db97db56de5f1226ca63de5ab425ff9453c4e46`

```dockerfile
```

-	Layers:
	-	`sha256:788a52ad55210bd2d4ed9fbbd6a152ba7b14dc3b7ee4c53d0f3a5cdedddf22d2`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5` - linux; arm variant v7

```console
$ docker pull docker@sha256:556db6b0e9df61bc612f019a8d4f6b5893969e89ddef9a58ffda03de01db0986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137322880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80105514d7c10daa8dcca6c73d62d0fcfcff8aef05f53027ed8f5b1e79221ea2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cbf04f008d9ef02dc799e294f7dfb15a6e1a7aa998c3ebd1abf85624fd8a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 7.4 MB (7437673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1a1cead3e82bc31db9d8227c36601c068da1b29538ac729dc38b62a255fa5`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73fe5fd8d6e91b61f554e5f4b6b205576d456d3ff11c7c7ae9f52c5dcbcb470`  
		Last Modified: Wed, 08 Oct 2025 20:23:28 GMT  
		Size: 18.4 MB (18402565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903fc967e46d7ed98ec9852c40659425d0fb55abfe4f3114b15a6d051a4c554f`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd58177b493833da3bb70027bbd00cd33ec2a6a6b37a4d8902ac62484e484b`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.4 MB (20352523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bada26e2a877a929758e22c849d20f156052c10b2613fc9122bf7b4e0d47050`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1b317dd5ec27fce62f574f1407e0d4893a1fe837e0e400de6dad22af04a1a`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35505dbf43402553e3b3c3b3c5f96a72c4772064bb797056463d77c9ced603d6`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cdb6aaff8e793882f2f2c50f51ed0c543232f7ab61ec1a55f57a7fff20e9fd`  
		Last Modified: Wed, 08 Oct 2025 20:54:16 GMT  
		Size: 8.6 MB (8610534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565524eb45b33cca7682947b28d97afa084eef35709cac083c7154e7ee93cb0`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 86.4 KB (86414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9137482da6d642b27169cbfe86fc0512df0e52ca658835c1e4a3354f9bdc05`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8654f9a663a2d9b3e893f06fd452e75bae44e486b46bd0acbf041c75356cfc5`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.5 MB (58461578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882f3a2fa1333d7ac2956f36df7b2ef37b65a14f4cd5a4a740b0bd54d1984e4`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509993fdecc5bd3d307dd22ffb54af7aebf642e0155a25d6035c07102dd71f5`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5` - unknown; unknown

```console
$ docker pull docker@sha256:2d13d67ca9ef63f5eae6bba37fa287fcd66f661a5ab7002efbc8cb272edf5e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49ceb1c2519c405e3dfb782a06e6b1843eafc37059e91f61f0dfb01d8e828b`

```dockerfile
```

-	Layers:
	-	`sha256:843f07fbd7ee6fd55be49dd57f9c2124b4545c2bfe2d8430d990874abce54d87`  
		Last Modified: Wed, 08 Oct 2025 23:07:39 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9449b06cd22f308c6da3438072219d67a8f97108a97592e085569dae2ccdfc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139518141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fb75ea8a70cd3e982f7092098519a9358044c47278398e2b0e6584159ff182`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb8af46f57d19a7eff37ee20d0f745f2b25c2db3b03f886c5a262a2f978a5e`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 8.2 MB (8227626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e992b003cff6ac506b5770b58db53b0f264a7863c746e93a526eda5371cbb67`  
		Last Modified: Wed, 08 Oct 2025 20:25:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad120ba60793ead7541cf11a93928a23a8096c556b455d71e627b4770101eaf`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.2 MB (19232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bffd5eefa70b71759fe0ba576c4e5a833cd108f5798c6b7a09fe803268b02a`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e293265a4a953b06a80ea42dcf65f5105661e35dcd4e3db9929129fcbaef9`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec633ce7cb5252722f81f70be756b95d7ece1d440cd03c2b8e47cc8e81c6f3`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebf8988ea011982152e9840872446a584f00fba937e96bcbeb387ad10c2aca`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34003f92833935910091b03a75c728b9d21498e4db1400fd148a1efe0657544b`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f803108a8d61186171f4e10fe37dc2d290ac0b06ea7697d287f65327d18754fe`  
		Last Modified: Wed, 08 Oct 2025 20:33:22 GMT  
		Size: 10.0 MB (10032583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf713f8b6955fe83fa08d31cd4c30540fd734f00883ec9c827b12637f1baddd`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 99.5 KB (99542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9df8ad4f1ac1a4a2e84cf23938b4fc4a9d2aa2cdf2f3a0ef3611e36bb5f90c`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe98abb3a4ed4d7df089ae860cee02629c5ad7d91820952b15b2965d109ee2`  
		Last Modified: Wed, 08 Oct 2025 20:33:26 GMT  
		Size: 57.8 MB (57758061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241f05e886b9dc02131bb575c75a464cd577a7a7e082f41993e2180d95dc367`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fff9ec4efe80e48bed7b9607d6734de8054195e33b010de9d037f452d0a03d`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 3.3 KB (3292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5` - unknown; unknown

```console
$ docker pull docker@sha256:b8efda5d1a7b765ec59ee503923e04d468f4202d8e4bd77ad5acc8ece82bfa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691659727245be56f7f4184be548de4c6f5841acc17ac30efe2d295503f06208`

```dockerfile
```

-	Layers:
	-	`sha256:1ea5e87c40e396c7f276887066b70aa11aa4cfabe79495c6ab35d902bb65a04b`  
		Last Modified: Wed, 08 Oct 2025 23:07:42 GMT  
		Size: 34.8 KB (34831 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5-cli`

```console
$ docker pull docker@sha256:19b6a32c14b2d71c0ef4575f6ad1712dca6f23f73155a60bb07c0d1f4fb00418
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

### `docker:28.5-cli` - linux; amd64

```console
$ docker pull docker@sha256:2ceaba2d9fe94568625978458a4f93e81b294fb96927fe2602b2cedd0bf9aea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76218700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6fa733b2ab715cbe441dd3c8359166d4973a32bd0dd734ee6ae29d4674c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f0a7b75fac3ac0bdc9c259b3dee99d1b76ee443dac8cfba8dd29f35c802a2c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faabc0adf6d1af8f9982e75c4aa3764cfb09e6b1e25ea0d359271125a065cdf`

```dockerfile
```

-	Layers:
	-	`sha256:c9a093a89c86df61de202e883b8edc52d7bda13f8a30db29a33e6bb0cd17fb1e`  
		Last Modified: Wed, 08 Oct 2025 23:07:49 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ee987cd4ffdfcf157a4df2756fe649bcf28040e3120405621f2106d5b95a65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71167610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8797fa6025da5f6cf43e5c7d5a861a13c1310981b47c73deaf111403fc763d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:913a776a1640e30a4787299519798eece3065c0a11f093478d4fd2729f8d09f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb92b7516dfaf1ff47deaa4c43d8c5da5e5d5a3063009bcbfaca11b0f4638e`

```dockerfile
```

-	Layers:
	-	`sha256:c6429b41ec7e43b858d6fc47cfbdf63b75084dd78f7a456a4109e8ef5fa7d9ae`  
		Last Modified: Wed, 08 Oct 2025 23:07:52 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ca49543195a1e53642ae43f301269504f6157911c85df2e1fe9a48f2b641a5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70160704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3864f57cedbc27d92173d6ce1ff98bd62deb24f2f012baa9bfd8c86bd18a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:27cfbd43240b2a36d9206e8d65ffa68cc828cc333dee94860ea8fe50fcdedc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54f87f9a325c1a28f3911b733bb8d436d5a344e5f4cab025423060c3122f12`

```dockerfile
```

-	Layers:
	-	`sha256:1c73b917de5769ed1585050836dd77eb606db44134e96525d7b6be3ce44aa0d5`  
		Last Modified: Wed, 08 Oct 2025 23:07:56 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a246a4a6c87424fc8e26fbd5f8f26e1ac19e2745da7e3c40be18b8c265ae1bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71629206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9625f7aa2680d221b2ee306d6dd46be38d361c45cde6e47d84115ebc8faa619c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b2a82343ac247cca758d9a1cf13ec29c7705a3d4f11eac33840976a005f375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcf6dab5064a1fd34f33a9e7a5856d82a8f5ae4eb063493a494c9439eda61ad`

```dockerfile
```

-	Layers:
	-	`sha256:7879f0a2aa84744862fb9b29e3a5a4bcf9495ec25822e20b5e68e59056b15992`  
		Last Modified: Wed, 08 Oct 2025 23:07:59 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5-dind`

```console
$ docker pull docker@sha256:7c3953162b1feca2aeb68a88ccb206485ff8c06177352ed9ffb3606354837869
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

### `docker:28.5-dind` - linux; amd64

```console
$ docker pull docker@sha256:17dd9c4154d3ca889b5b31e3e4b2818645819996f456e6c3e17b581737a44640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148653816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6219f96c48a526ca01fa59e2eca65ec67cd3f979f6c48dedeb14e6697dc42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0774022190f2b752e87a84c66b9a6ff1b3bbae43c893a860bd9a3fcbc4290ca`  
		Last Modified: Wed, 08 Oct 2025 20:34:07 GMT  
		Size: 9.5 MB (9507816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a691ee9764b4b3f4d9affb8c29ffc03f4c4d989298e2b2bfb93f4331b46f7`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a961a73cdd2322e8f59b2d11b5b5f03c41e6e488e12cb58d8a99bd02721ba90`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eaed86521d704b815068678197393163d0e1dc0dacde55392442b31b2bd192`  
		Last Modified: Wed, 08 Oct 2025 20:34:13 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49f61d997913f33514036426a2065cebcfafe63fa9d6464806bab8cff14914`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4b3e1409309a4af29d18da4edc4d1e06493028905509bce28eab52f2830e2`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:83e9d11602839d96665359ff81acf502ca43128754c722e7e02d5485220c97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ebaedf942d951b446ca1d48457cc7c468773b27f124b9f82e2761ec02af24`

```dockerfile
```

-	Layers:
	-	`sha256:60b958c4eb2101a33fd57b379ecb3eaddf7b960fa6558ae1e09fc807a11af41b`  
		Last Modified: Wed, 08 Oct 2025 23:07:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:23a94b59cfc54fb3f0a85562f77e1976ae427b6702eda1a6cc05665877ea7b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139351050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ad2dd9699bda1ab2c7d47dae8a76a2b693177a5f21a4d6ce52b8b5d54dc3f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7287652ad0f7417ae457a402f40a248670eddecae812df05328d7506b4eb7e`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 8.1 MB (8113337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431c8dbca316340be018038caec6bbb46de520002d7da495df2f3e22849718e`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2563734e87d4a41e756c5736d441c0d579cf5894976488bda29c158ca7b63c`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 18.4 MB (18418117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a98f22f147edc4650160e65326ae9aba04a825e888134bed99a30de9924eec`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e91a5ae2992f9361c096f7b969cbecfda20fe4c12e9c334d78dd56773286d8`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.4 MB (20371581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a13a1e08f9cd1e0584b24d8da93cf0b6f5047eeaf877caab0f4e47c1995081`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ecb3b6457a07ed0380f10034b6b0c3debcedce2a293f27f758b11cea20773f`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfb0083d4b0f462cdd77af85a4fc4fa2a17d49e30ec95f875998c1f8e27c759`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f97c4423935104b21120f03a4a4115af7e34c6549f33ba3f728f62acd6d3f8`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 9.5 MB (9461590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f59d52b9ff498c398252d10538d93ccda3c0928772008c1888f81cb9d58194f`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 90.0 KB (89976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555d288334111b4ea28df2e84d6e78b4a9351fef638dc5b83b1627892ede34c`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de61bedb5fac1b2191c9f3ab0f3dffca84f002acff72b937d528ff96cbf4d14`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.6 MB (58629069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e881d9a90366a6825183c33b18cb2464e9c0ba0ecb7195e91e15ab09201a7`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a5c01ee4ee6468b4679313e14ac47b9ae9211a3a82b2c619a88f3d050eda0a`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6e1b8fdc4984c0332556dbbf675047c01e0dc730a44ba6a1d254bc3bfb80e104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486c5363be4c09b70896b0b3db97db56de5f1226ca63de5ab425ff9453c4e46`

```dockerfile
```

-	Layers:
	-	`sha256:788a52ad55210bd2d4ed9fbbd6a152ba7b14dc3b7ee4c53d0f3a5cdedddf22d2`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:556db6b0e9df61bc612f019a8d4f6b5893969e89ddef9a58ffda03de01db0986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137322880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80105514d7c10daa8dcca6c73d62d0fcfcff8aef05f53027ed8f5b1e79221ea2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cbf04f008d9ef02dc799e294f7dfb15a6e1a7aa998c3ebd1abf85624fd8a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 7.4 MB (7437673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1a1cead3e82bc31db9d8227c36601c068da1b29538ac729dc38b62a255fa5`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73fe5fd8d6e91b61f554e5f4b6b205576d456d3ff11c7c7ae9f52c5dcbcb470`  
		Last Modified: Wed, 08 Oct 2025 20:23:28 GMT  
		Size: 18.4 MB (18402565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903fc967e46d7ed98ec9852c40659425d0fb55abfe4f3114b15a6d051a4c554f`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd58177b493833da3bb70027bbd00cd33ec2a6a6b37a4d8902ac62484e484b`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.4 MB (20352523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bada26e2a877a929758e22c849d20f156052c10b2613fc9122bf7b4e0d47050`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1b317dd5ec27fce62f574f1407e0d4893a1fe837e0e400de6dad22af04a1a`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35505dbf43402553e3b3c3b3c5f96a72c4772064bb797056463d77c9ced603d6`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cdb6aaff8e793882f2f2c50f51ed0c543232f7ab61ec1a55f57a7fff20e9fd`  
		Last Modified: Wed, 08 Oct 2025 20:54:16 GMT  
		Size: 8.6 MB (8610534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565524eb45b33cca7682947b28d97afa084eef35709cac083c7154e7ee93cb0`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 86.4 KB (86414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9137482da6d642b27169cbfe86fc0512df0e52ca658835c1e4a3354f9bdc05`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8654f9a663a2d9b3e893f06fd452e75bae44e486b46bd0acbf041c75356cfc5`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.5 MB (58461578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882f3a2fa1333d7ac2956f36df7b2ef37b65a14f4cd5a4a740b0bd54d1984e4`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509993fdecc5bd3d307dd22ffb54af7aebf642e0155a25d6035c07102dd71f5`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2d13d67ca9ef63f5eae6bba37fa287fcd66f661a5ab7002efbc8cb272edf5e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49ceb1c2519c405e3dfb782a06e6b1843eafc37059e91f61f0dfb01d8e828b`

```dockerfile
```

-	Layers:
	-	`sha256:843f07fbd7ee6fd55be49dd57f9c2124b4545c2bfe2d8430d990874abce54d87`  
		Last Modified: Wed, 08 Oct 2025 23:07:39 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9449b06cd22f308c6da3438072219d67a8f97108a97592e085569dae2ccdfc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139518141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fb75ea8a70cd3e982f7092098519a9358044c47278398e2b0e6584159ff182`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb8af46f57d19a7eff37ee20d0f745f2b25c2db3b03f886c5a262a2f978a5e`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 8.2 MB (8227626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e992b003cff6ac506b5770b58db53b0f264a7863c746e93a526eda5371cbb67`  
		Last Modified: Wed, 08 Oct 2025 20:25:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad120ba60793ead7541cf11a93928a23a8096c556b455d71e627b4770101eaf`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.2 MB (19232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bffd5eefa70b71759fe0ba576c4e5a833cd108f5798c6b7a09fe803268b02a`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e293265a4a953b06a80ea42dcf65f5105661e35dcd4e3db9929129fcbaef9`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec633ce7cb5252722f81f70be756b95d7ece1d440cd03c2b8e47cc8e81c6f3`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebf8988ea011982152e9840872446a584f00fba937e96bcbeb387ad10c2aca`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34003f92833935910091b03a75c728b9d21498e4db1400fd148a1efe0657544b`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f803108a8d61186171f4e10fe37dc2d290ac0b06ea7697d287f65327d18754fe`  
		Last Modified: Wed, 08 Oct 2025 20:33:22 GMT  
		Size: 10.0 MB (10032583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf713f8b6955fe83fa08d31cd4c30540fd734f00883ec9c827b12637f1baddd`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 99.5 KB (99542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9df8ad4f1ac1a4a2e84cf23938b4fc4a9d2aa2cdf2f3a0ef3611e36bb5f90c`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe98abb3a4ed4d7df089ae860cee02629c5ad7d91820952b15b2965d109ee2`  
		Last Modified: Wed, 08 Oct 2025 20:33:26 GMT  
		Size: 57.8 MB (57758061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241f05e886b9dc02131bb575c75a464cd577a7a7e082f41993e2180d95dc367`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fff9ec4efe80e48bed7b9607d6734de8054195e33b010de9d037f452d0a03d`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 3.3 KB (3292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b8efda5d1a7b765ec59ee503923e04d468f4202d8e4bd77ad5acc8ece82bfa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691659727245be56f7f4184be548de4c6f5841acc17ac30efe2d295503f06208`

```dockerfile
```

-	Layers:
	-	`sha256:1ea5e87c40e396c7f276887066b70aa11aa4cfabe79495c6ab35d902bb65a04b`  
		Last Modified: Wed, 08 Oct 2025 23:07:42 GMT  
		Size: 34.8 KB (34831 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5-dind-rootless`

```console
$ docker pull docker@sha256:eeb43ad630a5165c910f03041a590147ddb1c2632be3a3c397e9b2c2b4efa7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.5-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:b3d53c924e34d7e003f601d8d6222844b9c1b71b7aa0b2ed4655a6b30fe32602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169675916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78479fdc55be9d0c2772a94ab8b66e905f686b58a754da0f12cd11b4ba460167`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD []
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f4121261305cd808f866e5cc468c62c7b691048458ce84c73cebc8744a0f5c`  
		Last Modified: Fri, 03 Oct 2025 15:42:57 GMT  
		Size: 8.2 MB (8206013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacb763c34fa98faf157ad30ac845055c7e17d6bc356a735dd34979b2ca3dcd`  
		Last Modified: Fri, 03 Oct 2025 15:42:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82baaa61b0bd5e833b9bf0dce2a5ba042e651d1dae98dcecd76a54d85245f705`  
		Last Modified: Fri, 03 Oct 2025 15:43:00 GMT  
		Size: 20.4 MB (20429721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c233148e55acfe21ab7559acf33645c62cab15c2786fb755b117d0f761692214`  
		Last Modified: Fri, 03 Oct 2025 15:43:04 GMT  
		Size: 22.2 MB (22158310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a01365128829f855670516e240e079aaa07cca78da2106a03fe8cc88723c3c6`  
		Last Modified: Fri, 03 Oct 2025 15:43:10 GMT  
		Size: 21.7 MB (21656766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d97b7b769f0ef0ffff5fb8721b8852aab640d625cccad858457c7ccdc01909`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252ca38c80c99c59f88eb9177337a5d1e1be51a71bca74077ce10d0e2db2ff6`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f710bb1cc914e30eac705c8d79e2b6fac559197d538c0a843bfdd992a69bfe1`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bd32a0ea96da36ee694f909a448f72d9ce8f3161366150204ce43f92f3ef25`  
		Last Modified: Fri, 03 Oct 2025 16:55:35 GMT  
		Size: 9.5 MB (9507812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b78db0b14600437995bb4b41a16d542cc1c29e47d131a154fcd0e71e1240e7`  
		Last Modified: Fri, 03 Oct 2025 16:33:46 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02844b1b965c7106b174fa8fcc81da5932ae550f52b2cdea2f4b1cbc72cf9103`  
		Last Modified: Fri, 03 Oct 2025 16:33:51 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c0d4f3fc3deda7540f99bf89eb4616d8fe2bf6fde04101d3c62817b55b32ed`  
		Last Modified: Fri, 03 Oct 2025 16:55:36 GMT  
		Size: 62.8 MB (62827332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2b4197469badf8d75becb38e327e689d7b466f9a06cbf2e22c1574489684fc`  
		Last Modified: Fri, 03 Oct 2025 16:33:54 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733f9fcc3eeee9d72d8b472b1225e3228f39f1cefe71d8dff9f1a2c710decce`  
		Last Modified: Fri, 03 Oct 2025 16:33:57 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac14d1bbef2a00ee6148a84da6d122959f4469478e896e6b0238d37228c12e58`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 3.4 MB (3398331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a4cba6aa490126672884ec1cc7fc81c87c39f7a7b752a3a27031de81cc7e66`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3068b13530be21c371198cff4b2617ff2f7bf794a5ff5f9daf01addd778aa4b0`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aed80e8577ba3b89d9e8425fc00a705532e626ca3fc051bad538409c0399762`  
		Last Modified: Fri, 03 Oct 2025 16:56:14 GMT  
		Size: 17.6 MB (17592032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069ff56a1905eb0680d22ee4587a1a1ba638f709814aca49b750b3c4bf3531f6`  
		Last Modified: Fri, 03 Oct 2025 16:56:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:93a89793da5adcc19ef3c9827d45c6ecb2767c1a1585dc874a34e2e3565f084f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119379607dbb4d2e6842aa149d585b6259e03e4b136a8b29a877d1fd94e7a05f`

```dockerfile
```

-	Layers:
	-	`sha256:91562a8e6c08e44f1300395f13fbf8c2f9e8521ccc3a5a2685e8553f477b409e`  
		Last Modified: Fri, 03 Oct 2025 17:07:59 GMT  
		Size: 30.6 KB (30636 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:96a3c2358a11eb6c0b8b8697af03c763b040a4289d5cdb41afce7cccfdc6a7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160960944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09fc28f780b87f424eac4f8d8e1a3e2f8b076509e298aa9f1c3af3ce13c6945`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD []
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befee8c2b0ad40f8afec285692dd9de306244ab77849362b32f364598f4dd856`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 8.2 MB (8227655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81db965703fb492a9487f0707728f846ca5016cffbe4cca14a9aaedf3fe47be`  
		Last Modified: Fri, 03 Oct 2025 16:10:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae023da43925318e9d906c7752c90968e4e76401eff1a13c13a02dfad260775`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 19.2 MB (19238158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d084ed095dcaaa56e75d1464d58172ca160961091fd6c2110b81301c1c8d144a`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 20.3 MB (20274240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5cbf3334db63fb72ebb37340a3158221d6151607e4b01c5be6b44f4c2a1f35`  
		Last Modified: Fri, 03 Oct 2025 16:10:10 GMT  
		Size: 19.8 MB (19779981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a37c322750556c7e8922a42c05e513ce640dbe5059b406843b4285c15f28be`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ee98d68b79d3a825b7c3d7d4492c505cae7e7ee829b8da41259b5372f704be`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06880fc24b1d74868cf537077a0bd0cc09b9cb315d6f2e5ba9ae3fe57405085f`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e663db0fdfaf3e5f40f7c3d7c3d51cfa62bbe43ddfcb4fe99cb8b6c637f6aa`  
		Last Modified: Fri, 03 Oct 2025 16:11:02 GMT  
		Size: 10.0 MB (10032639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5e31e2508033fa71a6e9c996b28c63fb8717b1fb04950cc9bf8ab9c496715c`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 99.6 KB (99551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44d97f98752505c225f3d7bf9a163d9522bb8c15f839dde10ca592bec612151`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db3a1adaf72d283f41dd82a794dd8a21401cf97b9547986d552142a747eb5ae`  
		Last Modified: Fri, 03 Oct 2025 16:11:06 GMT  
		Size: 57.8 MB (57759208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0ea7e65ba6a9a348e2c362f6ee2128c9cbbc4fe766157fac25a52324ef2e0c`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8003cd90da085be86d46c270b3ffed416d670d6fb46dc211845eaad27c21794`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210fc14d10dd6889f85a6c0dda51131547e11a4b09c342a41f267e3b05025bb`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 3.4 MB (3389873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650ea26cdb1e4676d6bce162d7e5a937b93e2705cc86380b54dd03d1e8b1abd3`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5728e12ff2b23e1c18b5c20970862362841a7011baa80aef4a45d5a1b108115`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30951d5b864c3c60fe2adf5433ff9e1d915fc52fdd40fae1766a1948ac8ef345`  
		Last Modified: Fri, 03 Oct 2025 17:08:19 GMT  
		Size: 18.0 MB (18019399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056d88955c46abf8014f4e3163803203a97c96513ab2783aee987fd1cc078700`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4025f450b00c6226d6682f17fbdaa8ff0aca575e36b82377be3680a70b1008ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd180d64e35b20ae847a8335cd5554d37b68ed547c4530d96e617dd92f1a9a0`

```dockerfile
```

-	Layers:
	-	`sha256:e94643b935420367d72f27be406ef5a64f8862ab497d1cb7c6291454821ec49c`  
		Last Modified: Fri, 03 Oct 2025 17:08:03 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5-windowsservercore`

```console
$ docker pull docker@sha256:337c819e1e92bbe665964fa9ff8420a91cd889d8b99ba336749af5eb20bd5502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.5-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:08fcf22b324f01b24d7d6c9edb2a077743fcb7a420e4263f0b1bca4952e41c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a850d0d3454900418bf8bd97acb002622a6ed5b1a77fa6fd76412b1f4f8ef768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:28.5-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5.1`

```console
$ docker pull docker@sha256:7c3953162b1feca2aeb68a88ccb206485ff8c06177352ed9ffb3606354837869
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

### `docker:28.5.1` - linux; amd64

```console
$ docker pull docker@sha256:17dd9c4154d3ca889b5b31e3e4b2818645819996f456e6c3e17b581737a44640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148653816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6219f96c48a526ca01fa59e2eca65ec67cd3f979f6c48dedeb14e6697dc42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0774022190f2b752e87a84c66b9a6ff1b3bbae43c893a860bd9a3fcbc4290ca`  
		Last Modified: Wed, 08 Oct 2025 20:34:07 GMT  
		Size: 9.5 MB (9507816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a691ee9764b4b3f4d9affb8c29ffc03f4c4d989298e2b2bfb93f4331b46f7`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a961a73cdd2322e8f59b2d11b5b5f03c41e6e488e12cb58d8a99bd02721ba90`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eaed86521d704b815068678197393163d0e1dc0dacde55392442b31b2bd192`  
		Last Modified: Wed, 08 Oct 2025 20:34:13 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49f61d997913f33514036426a2065cebcfafe63fa9d6464806bab8cff14914`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4b3e1409309a4af29d18da4edc4d1e06493028905509bce28eab52f2830e2`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1` - unknown; unknown

```console
$ docker pull docker@sha256:83e9d11602839d96665359ff81acf502ca43128754c722e7e02d5485220c97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ebaedf942d951b446ca1d48457cc7c468773b27f124b9f82e2761ec02af24`

```dockerfile
```

-	Layers:
	-	`sha256:60b958c4eb2101a33fd57b379ecb3eaddf7b960fa6558ae1e09fc807a11af41b`  
		Last Modified: Wed, 08 Oct 2025 23:07:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:23a94b59cfc54fb3f0a85562f77e1976ae427b6702eda1a6cc05665877ea7b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139351050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ad2dd9699bda1ab2c7d47dae8a76a2b693177a5f21a4d6ce52b8b5d54dc3f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7287652ad0f7417ae457a402f40a248670eddecae812df05328d7506b4eb7e`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 8.1 MB (8113337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431c8dbca316340be018038caec6bbb46de520002d7da495df2f3e22849718e`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2563734e87d4a41e756c5736d441c0d579cf5894976488bda29c158ca7b63c`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 18.4 MB (18418117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a98f22f147edc4650160e65326ae9aba04a825e888134bed99a30de9924eec`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e91a5ae2992f9361c096f7b969cbecfda20fe4c12e9c334d78dd56773286d8`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.4 MB (20371581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a13a1e08f9cd1e0584b24d8da93cf0b6f5047eeaf877caab0f4e47c1995081`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ecb3b6457a07ed0380f10034b6b0c3debcedce2a293f27f758b11cea20773f`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfb0083d4b0f462cdd77af85a4fc4fa2a17d49e30ec95f875998c1f8e27c759`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f97c4423935104b21120f03a4a4115af7e34c6549f33ba3f728f62acd6d3f8`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 9.5 MB (9461590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f59d52b9ff498c398252d10538d93ccda3c0928772008c1888f81cb9d58194f`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 90.0 KB (89976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555d288334111b4ea28df2e84d6e78b4a9351fef638dc5b83b1627892ede34c`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de61bedb5fac1b2191c9f3ab0f3dffca84f002acff72b937d528ff96cbf4d14`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.6 MB (58629069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e881d9a90366a6825183c33b18cb2464e9c0ba0ecb7195e91e15ab09201a7`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a5c01ee4ee6468b4679313e14ac47b9ae9211a3a82b2c619a88f3d050eda0a`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1` - unknown; unknown

```console
$ docker pull docker@sha256:6e1b8fdc4984c0332556dbbf675047c01e0dc730a44ba6a1d254bc3bfb80e104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486c5363be4c09b70896b0b3db97db56de5f1226ca63de5ab425ff9453c4e46`

```dockerfile
```

-	Layers:
	-	`sha256:788a52ad55210bd2d4ed9fbbd6a152ba7b14dc3b7ee4c53d0f3a5cdedddf22d2`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:556db6b0e9df61bc612f019a8d4f6b5893969e89ddef9a58ffda03de01db0986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137322880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80105514d7c10daa8dcca6c73d62d0fcfcff8aef05f53027ed8f5b1e79221ea2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cbf04f008d9ef02dc799e294f7dfb15a6e1a7aa998c3ebd1abf85624fd8a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 7.4 MB (7437673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1a1cead3e82bc31db9d8227c36601c068da1b29538ac729dc38b62a255fa5`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73fe5fd8d6e91b61f554e5f4b6b205576d456d3ff11c7c7ae9f52c5dcbcb470`  
		Last Modified: Wed, 08 Oct 2025 20:23:28 GMT  
		Size: 18.4 MB (18402565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903fc967e46d7ed98ec9852c40659425d0fb55abfe4f3114b15a6d051a4c554f`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd58177b493833da3bb70027bbd00cd33ec2a6a6b37a4d8902ac62484e484b`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.4 MB (20352523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bada26e2a877a929758e22c849d20f156052c10b2613fc9122bf7b4e0d47050`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1b317dd5ec27fce62f574f1407e0d4893a1fe837e0e400de6dad22af04a1a`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35505dbf43402553e3b3c3b3c5f96a72c4772064bb797056463d77c9ced603d6`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cdb6aaff8e793882f2f2c50f51ed0c543232f7ab61ec1a55f57a7fff20e9fd`  
		Last Modified: Wed, 08 Oct 2025 20:54:16 GMT  
		Size: 8.6 MB (8610534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565524eb45b33cca7682947b28d97afa084eef35709cac083c7154e7ee93cb0`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 86.4 KB (86414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9137482da6d642b27169cbfe86fc0512df0e52ca658835c1e4a3354f9bdc05`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8654f9a663a2d9b3e893f06fd452e75bae44e486b46bd0acbf041c75356cfc5`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.5 MB (58461578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882f3a2fa1333d7ac2956f36df7b2ef37b65a14f4cd5a4a740b0bd54d1984e4`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509993fdecc5bd3d307dd22ffb54af7aebf642e0155a25d6035c07102dd71f5`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1` - unknown; unknown

```console
$ docker pull docker@sha256:2d13d67ca9ef63f5eae6bba37fa287fcd66f661a5ab7002efbc8cb272edf5e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49ceb1c2519c405e3dfb782a06e6b1843eafc37059e91f61f0dfb01d8e828b`

```dockerfile
```

-	Layers:
	-	`sha256:843f07fbd7ee6fd55be49dd57f9c2124b4545c2bfe2d8430d990874abce54d87`  
		Last Modified: Wed, 08 Oct 2025 23:07:39 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9449b06cd22f308c6da3438072219d67a8f97108a97592e085569dae2ccdfc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139518141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fb75ea8a70cd3e982f7092098519a9358044c47278398e2b0e6584159ff182`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb8af46f57d19a7eff37ee20d0f745f2b25c2db3b03f886c5a262a2f978a5e`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 8.2 MB (8227626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e992b003cff6ac506b5770b58db53b0f264a7863c746e93a526eda5371cbb67`  
		Last Modified: Wed, 08 Oct 2025 20:25:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad120ba60793ead7541cf11a93928a23a8096c556b455d71e627b4770101eaf`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.2 MB (19232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bffd5eefa70b71759fe0ba576c4e5a833cd108f5798c6b7a09fe803268b02a`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e293265a4a953b06a80ea42dcf65f5105661e35dcd4e3db9929129fcbaef9`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec633ce7cb5252722f81f70be756b95d7ece1d440cd03c2b8e47cc8e81c6f3`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebf8988ea011982152e9840872446a584f00fba937e96bcbeb387ad10c2aca`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34003f92833935910091b03a75c728b9d21498e4db1400fd148a1efe0657544b`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f803108a8d61186171f4e10fe37dc2d290ac0b06ea7697d287f65327d18754fe`  
		Last Modified: Wed, 08 Oct 2025 20:33:22 GMT  
		Size: 10.0 MB (10032583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf713f8b6955fe83fa08d31cd4c30540fd734f00883ec9c827b12637f1baddd`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 99.5 KB (99542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9df8ad4f1ac1a4a2e84cf23938b4fc4a9d2aa2cdf2f3a0ef3611e36bb5f90c`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe98abb3a4ed4d7df089ae860cee02629c5ad7d91820952b15b2965d109ee2`  
		Last Modified: Wed, 08 Oct 2025 20:33:26 GMT  
		Size: 57.8 MB (57758061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241f05e886b9dc02131bb575c75a464cd577a7a7e082f41993e2180d95dc367`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fff9ec4efe80e48bed7b9607d6734de8054195e33b010de9d037f452d0a03d`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 3.3 KB (3292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1` - unknown; unknown

```console
$ docker pull docker@sha256:b8efda5d1a7b765ec59ee503923e04d468f4202d8e4bd77ad5acc8ece82bfa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691659727245be56f7f4184be548de4c6f5841acc17ac30efe2d295503f06208`

```dockerfile
```

-	Layers:
	-	`sha256:1ea5e87c40e396c7f276887066b70aa11aa4cfabe79495c6ab35d902bb65a04b`  
		Last Modified: Wed, 08 Oct 2025 23:07:42 GMT  
		Size: 34.8 KB (34831 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-alpine3.22`

```console
$ docker pull docker@sha256:7c3953162b1feca2aeb68a88ccb206485ff8c06177352ed9ffb3606354837869
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

### `docker:28.5.1-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:17dd9c4154d3ca889b5b31e3e4b2818645819996f456e6c3e17b581737a44640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148653816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6219f96c48a526ca01fa59e2eca65ec67cd3f979f6c48dedeb14e6697dc42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0774022190f2b752e87a84c66b9a6ff1b3bbae43c893a860bd9a3fcbc4290ca`  
		Last Modified: Wed, 08 Oct 2025 20:34:07 GMT  
		Size: 9.5 MB (9507816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a691ee9764b4b3f4d9affb8c29ffc03f4c4d989298e2b2bfb93f4331b46f7`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a961a73cdd2322e8f59b2d11b5b5f03c41e6e488e12cb58d8a99bd02721ba90`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eaed86521d704b815068678197393163d0e1dc0dacde55392442b31b2bd192`  
		Last Modified: Wed, 08 Oct 2025 20:34:13 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49f61d997913f33514036426a2065cebcfafe63fa9d6464806bab8cff14914`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4b3e1409309a4af29d18da4edc4d1e06493028905509bce28eab52f2830e2`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:83e9d11602839d96665359ff81acf502ca43128754c722e7e02d5485220c97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ebaedf942d951b446ca1d48457cc7c468773b27f124b9f82e2761ec02af24`

```dockerfile
```

-	Layers:
	-	`sha256:60b958c4eb2101a33fd57b379ecb3eaddf7b960fa6558ae1e09fc807a11af41b`  
		Last Modified: Wed, 08 Oct 2025 23:07:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:23a94b59cfc54fb3f0a85562f77e1976ae427b6702eda1a6cc05665877ea7b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139351050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ad2dd9699bda1ab2c7d47dae8a76a2b693177a5f21a4d6ce52b8b5d54dc3f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7287652ad0f7417ae457a402f40a248670eddecae812df05328d7506b4eb7e`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 8.1 MB (8113337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431c8dbca316340be018038caec6bbb46de520002d7da495df2f3e22849718e`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2563734e87d4a41e756c5736d441c0d579cf5894976488bda29c158ca7b63c`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 18.4 MB (18418117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a98f22f147edc4650160e65326ae9aba04a825e888134bed99a30de9924eec`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e91a5ae2992f9361c096f7b969cbecfda20fe4c12e9c334d78dd56773286d8`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.4 MB (20371581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a13a1e08f9cd1e0584b24d8da93cf0b6f5047eeaf877caab0f4e47c1995081`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ecb3b6457a07ed0380f10034b6b0c3debcedce2a293f27f758b11cea20773f`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfb0083d4b0f462cdd77af85a4fc4fa2a17d49e30ec95f875998c1f8e27c759`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f97c4423935104b21120f03a4a4115af7e34c6549f33ba3f728f62acd6d3f8`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 9.5 MB (9461590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f59d52b9ff498c398252d10538d93ccda3c0928772008c1888f81cb9d58194f`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 90.0 KB (89976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555d288334111b4ea28df2e84d6e78b4a9351fef638dc5b83b1627892ede34c`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de61bedb5fac1b2191c9f3ab0f3dffca84f002acff72b937d528ff96cbf4d14`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.6 MB (58629069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e881d9a90366a6825183c33b18cb2464e9c0ba0ecb7195e91e15ab09201a7`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a5c01ee4ee6468b4679313e14ac47b9ae9211a3a82b2c619a88f3d050eda0a`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6e1b8fdc4984c0332556dbbf675047c01e0dc730a44ba6a1d254bc3bfb80e104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486c5363be4c09b70896b0b3db97db56de5f1226ca63de5ab425ff9453c4e46`

```dockerfile
```

-	Layers:
	-	`sha256:788a52ad55210bd2d4ed9fbbd6a152ba7b14dc3b7ee4c53d0f3a5cdedddf22d2`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:556db6b0e9df61bc612f019a8d4f6b5893969e89ddef9a58ffda03de01db0986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137322880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80105514d7c10daa8dcca6c73d62d0fcfcff8aef05f53027ed8f5b1e79221ea2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cbf04f008d9ef02dc799e294f7dfb15a6e1a7aa998c3ebd1abf85624fd8a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 7.4 MB (7437673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1a1cead3e82bc31db9d8227c36601c068da1b29538ac729dc38b62a255fa5`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73fe5fd8d6e91b61f554e5f4b6b205576d456d3ff11c7c7ae9f52c5dcbcb470`  
		Last Modified: Wed, 08 Oct 2025 20:23:28 GMT  
		Size: 18.4 MB (18402565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903fc967e46d7ed98ec9852c40659425d0fb55abfe4f3114b15a6d051a4c554f`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd58177b493833da3bb70027bbd00cd33ec2a6a6b37a4d8902ac62484e484b`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.4 MB (20352523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bada26e2a877a929758e22c849d20f156052c10b2613fc9122bf7b4e0d47050`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1b317dd5ec27fce62f574f1407e0d4893a1fe837e0e400de6dad22af04a1a`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35505dbf43402553e3b3c3b3c5f96a72c4772064bb797056463d77c9ced603d6`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cdb6aaff8e793882f2f2c50f51ed0c543232f7ab61ec1a55f57a7fff20e9fd`  
		Last Modified: Wed, 08 Oct 2025 20:54:16 GMT  
		Size: 8.6 MB (8610534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565524eb45b33cca7682947b28d97afa084eef35709cac083c7154e7ee93cb0`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 86.4 KB (86414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9137482da6d642b27169cbfe86fc0512df0e52ca658835c1e4a3354f9bdc05`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8654f9a663a2d9b3e893f06fd452e75bae44e486b46bd0acbf041c75356cfc5`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.5 MB (58461578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882f3a2fa1333d7ac2956f36df7b2ef37b65a14f4cd5a4a740b0bd54d1984e4`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509993fdecc5bd3d307dd22ffb54af7aebf642e0155a25d6035c07102dd71f5`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:2d13d67ca9ef63f5eae6bba37fa287fcd66f661a5ab7002efbc8cb272edf5e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49ceb1c2519c405e3dfb782a06e6b1843eafc37059e91f61f0dfb01d8e828b`

```dockerfile
```

-	Layers:
	-	`sha256:843f07fbd7ee6fd55be49dd57f9c2124b4545c2bfe2d8430d990874abce54d87`  
		Last Modified: Wed, 08 Oct 2025 23:07:39 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9449b06cd22f308c6da3438072219d67a8f97108a97592e085569dae2ccdfc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139518141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fb75ea8a70cd3e982f7092098519a9358044c47278398e2b0e6584159ff182`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb8af46f57d19a7eff37ee20d0f745f2b25c2db3b03f886c5a262a2f978a5e`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 8.2 MB (8227626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e992b003cff6ac506b5770b58db53b0f264a7863c746e93a526eda5371cbb67`  
		Last Modified: Wed, 08 Oct 2025 20:25:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad120ba60793ead7541cf11a93928a23a8096c556b455d71e627b4770101eaf`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.2 MB (19232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bffd5eefa70b71759fe0ba576c4e5a833cd108f5798c6b7a09fe803268b02a`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e293265a4a953b06a80ea42dcf65f5105661e35dcd4e3db9929129fcbaef9`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec633ce7cb5252722f81f70be756b95d7ece1d440cd03c2b8e47cc8e81c6f3`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebf8988ea011982152e9840872446a584f00fba937e96bcbeb387ad10c2aca`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34003f92833935910091b03a75c728b9d21498e4db1400fd148a1efe0657544b`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f803108a8d61186171f4e10fe37dc2d290ac0b06ea7697d287f65327d18754fe`  
		Last Modified: Wed, 08 Oct 2025 20:33:22 GMT  
		Size: 10.0 MB (10032583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf713f8b6955fe83fa08d31cd4c30540fd734f00883ec9c827b12637f1baddd`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 99.5 KB (99542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9df8ad4f1ac1a4a2e84cf23938b4fc4a9d2aa2cdf2f3a0ef3611e36bb5f90c`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe98abb3a4ed4d7df089ae860cee02629c5ad7d91820952b15b2965d109ee2`  
		Last Modified: Wed, 08 Oct 2025 20:33:26 GMT  
		Size: 57.8 MB (57758061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241f05e886b9dc02131bb575c75a464cd577a7a7e082f41993e2180d95dc367`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fff9ec4efe80e48bed7b9607d6734de8054195e33b010de9d037f452d0a03d`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 3.3 KB (3292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:b8efda5d1a7b765ec59ee503923e04d468f4202d8e4bd77ad5acc8ece82bfa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691659727245be56f7f4184be548de4c6f5841acc17ac30efe2d295503f06208`

```dockerfile
```

-	Layers:
	-	`sha256:1ea5e87c40e396c7f276887066b70aa11aa4cfabe79495c6ab35d902bb65a04b`  
		Last Modified: Wed, 08 Oct 2025 23:07:42 GMT  
		Size: 34.8 KB (34831 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-cli`

```console
$ docker pull docker@sha256:19b6a32c14b2d71c0ef4575f6ad1712dca6f23f73155a60bb07c0d1f4fb00418
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

### `docker:28.5.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:2ceaba2d9fe94568625978458a4f93e81b294fb96927fe2602b2cedd0bf9aea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76218700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6fa733b2ab715cbe441dd3c8359166d4973a32bd0dd734ee6ae29d4674c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f0a7b75fac3ac0bdc9c259b3dee99d1b76ee443dac8cfba8dd29f35c802a2c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faabc0adf6d1af8f9982e75c4aa3764cfb09e6b1e25ea0d359271125a065cdf`

```dockerfile
```

-	Layers:
	-	`sha256:c9a093a89c86df61de202e883b8edc52d7bda13f8a30db29a33e6bb0cd17fb1e`  
		Last Modified: Wed, 08 Oct 2025 23:07:49 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ee987cd4ffdfcf157a4df2756fe649bcf28040e3120405621f2106d5b95a65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71167610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8797fa6025da5f6cf43e5c7d5a861a13c1310981b47c73deaf111403fc763d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:913a776a1640e30a4787299519798eece3065c0a11f093478d4fd2729f8d09f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb92b7516dfaf1ff47deaa4c43d8c5da5e5d5a3063009bcbfaca11b0f4638e`

```dockerfile
```

-	Layers:
	-	`sha256:c6429b41ec7e43b858d6fc47cfbdf63b75084dd78f7a456a4109e8ef5fa7d9ae`  
		Last Modified: Wed, 08 Oct 2025 23:07:52 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ca49543195a1e53642ae43f301269504f6157911c85df2e1fe9a48f2b641a5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70160704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3864f57cedbc27d92173d6ce1ff98bd62deb24f2f012baa9bfd8c86bd18a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:27cfbd43240b2a36d9206e8d65ffa68cc828cc333dee94860ea8fe50fcdedc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54f87f9a325c1a28f3911b733bb8d436d5a344e5f4cab025423060c3122f12`

```dockerfile
```

-	Layers:
	-	`sha256:1c73b917de5769ed1585050836dd77eb606db44134e96525d7b6be3ce44aa0d5`  
		Last Modified: Wed, 08 Oct 2025 23:07:56 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a246a4a6c87424fc8e26fbd5f8f26e1ac19e2745da7e3c40be18b8c265ae1bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71629206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9625f7aa2680d221b2ee306d6dd46be38d361c45cde6e47d84115ebc8faa619c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b2a82343ac247cca758d9a1cf13ec29c7705a3d4f11eac33840976a005f375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcf6dab5064a1fd34f33a9e7a5856d82a8f5ae4eb063493a494c9439eda61ad`

```dockerfile
```

-	Layers:
	-	`sha256:7879f0a2aa84744862fb9b29e3a5a4bcf9495ec25822e20b5e68e59056b15992`  
		Last Modified: Wed, 08 Oct 2025 23:07:59 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-cli-alpine3.22`

```console
$ docker pull docker@sha256:19b6a32c14b2d71c0ef4575f6ad1712dca6f23f73155a60bb07c0d1f4fb00418
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

### `docker:28.5.1-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:2ceaba2d9fe94568625978458a4f93e81b294fb96927fe2602b2cedd0bf9aea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76218700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6fa733b2ab715cbe441dd3c8359166d4973a32bd0dd734ee6ae29d4674c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f0a7b75fac3ac0bdc9c259b3dee99d1b76ee443dac8cfba8dd29f35c802a2c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faabc0adf6d1af8f9982e75c4aa3764cfb09e6b1e25ea0d359271125a065cdf`

```dockerfile
```

-	Layers:
	-	`sha256:c9a093a89c86df61de202e883b8edc52d7bda13f8a30db29a33e6bb0cd17fb1e`  
		Last Modified: Wed, 08 Oct 2025 23:07:49 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ee987cd4ffdfcf157a4df2756fe649bcf28040e3120405621f2106d5b95a65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71167610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8797fa6025da5f6cf43e5c7d5a861a13c1310981b47c73deaf111403fc763d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:913a776a1640e30a4787299519798eece3065c0a11f093478d4fd2729f8d09f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb92b7516dfaf1ff47deaa4c43d8c5da5e5d5a3063009bcbfaca11b0f4638e`

```dockerfile
```

-	Layers:
	-	`sha256:c6429b41ec7e43b858d6fc47cfbdf63b75084dd78f7a456a4109e8ef5fa7d9ae`  
		Last Modified: Wed, 08 Oct 2025 23:07:52 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:ca49543195a1e53642ae43f301269504f6157911c85df2e1fe9a48f2b641a5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70160704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3864f57cedbc27d92173d6ce1ff98bd62deb24f2f012baa9bfd8c86bd18a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:27cfbd43240b2a36d9206e8d65ffa68cc828cc333dee94860ea8fe50fcdedc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54f87f9a325c1a28f3911b733bb8d436d5a344e5f4cab025423060c3122f12`

```dockerfile
```

-	Layers:
	-	`sha256:1c73b917de5769ed1585050836dd77eb606db44134e96525d7b6be3ce44aa0d5`  
		Last Modified: Wed, 08 Oct 2025 23:07:56 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a246a4a6c87424fc8e26fbd5f8f26e1ac19e2745da7e3c40be18b8c265ae1bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71629206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9625f7aa2680d221b2ee306d6dd46be38d361c45cde6e47d84115ebc8faa619c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:4b2a82343ac247cca758d9a1cf13ec29c7705a3d4f11eac33840976a005f375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcf6dab5064a1fd34f33a9e7a5856d82a8f5ae4eb063493a494c9439eda61ad`

```dockerfile
```

-	Layers:
	-	`sha256:7879f0a2aa84744862fb9b29e3a5a4bcf9495ec25822e20b5e68e59056b15992`  
		Last Modified: Wed, 08 Oct 2025 23:07:59 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-dind`

```console
$ docker pull docker@sha256:7c3953162b1feca2aeb68a88ccb206485ff8c06177352ed9ffb3606354837869
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

### `docker:28.5.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:17dd9c4154d3ca889b5b31e3e4b2818645819996f456e6c3e17b581737a44640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148653816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6219f96c48a526ca01fa59e2eca65ec67cd3f979f6c48dedeb14e6697dc42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0774022190f2b752e87a84c66b9a6ff1b3bbae43c893a860bd9a3fcbc4290ca`  
		Last Modified: Wed, 08 Oct 2025 20:34:07 GMT  
		Size: 9.5 MB (9507816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a691ee9764b4b3f4d9affb8c29ffc03f4c4d989298e2b2bfb93f4331b46f7`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a961a73cdd2322e8f59b2d11b5b5f03c41e6e488e12cb58d8a99bd02721ba90`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eaed86521d704b815068678197393163d0e1dc0dacde55392442b31b2bd192`  
		Last Modified: Wed, 08 Oct 2025 20:34:13 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49f61d997913f33514036426a2065cebcfafe63fa9d6464806bab8cff14914`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4b3e1409309a4af29d18da4edc4d1e06493028905509bce28eab52f2830e2`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:83e9d11602839d96665359ff81acf502ca43128754c722e7e02d5485220c97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ebaedf942d951b446ca1d48457cc7c468773b27f124b9f82e2761ec02af24`

```dockerfile
```

-	Layers:
	-	`sha256:60b958c4eb2101a33fd57b379ecb3eaddf7b960fa6558ae1e09fc807a11af41b`  
		Last Modified: Wed, 08 Oct 2025 23:07:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:23a94b59cfc54fb3f0a85562f77e1976ae427b6702eda1a6cc05665877ea7b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139351050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ad2dd9699bda1ab2c7d47dae8a76a2b693177a5f21a4d6ce52b8b5d54dc3f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7287652ad0f7417ae457a402f40a248670eddecae812df05328d7506b4eb7e`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 8.1 MB (8113337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431c8dbca316340be018038caec6bbb46de520002d7da495df2f3e22849718e`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2563734e87d4a41e756c5736d441c0d579cf5894976488bda29c158ca7b63c`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 18.4 MB (18418117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a98f22f147edc4650160e65326ae9aba04a825e888134bed99a30de9924eec`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e91a5ae2992f9361c096f7b969cbecfda20fe4c12e9c334d78dd56773286d8`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.4 MB (20371581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a13a1e08f9cd1e0584b24d8da93cf0b6f5047eeaf877caab0f4e47c1995081`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ecb3b6457a07ed0380f10034b6b0c3debcedce2a293f27f758b11cea20773f`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfb0083d4b0f462cdd77af85a4fc4fa2a17d49e30ec95f875998c1f8e27c759`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f97c4423935104b21120f03a4a4115af7e34c6549f33ba3f728f62acd6d3f8`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 9.5 MB (9461590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f59d52b9ff498c398252d10538d93ccda3c0928772008c1888f81cb9d58194f`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 90.0 KB (89976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555d288334111b4ea28df2e84d6e78b4a9351fef638dc5b83b1627892ede34c`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de61bedb5fac1b2191c9f3ab0f3dffca84f002acff72b937d528ff96cbf4d14`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.6 MB (58629069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e881d9a90366a6825183c33b18cb2464e9c0ba0ecb7195e91e15ab09201a7`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a5c01ee4ee6468b4679313e14ac47b9ae9211a3a82b2c619a88f3d050eda0a`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6e1b8fdc4984c0332556dbbf675047c01e0dc730a44ba6a1d254bc3bfb80e104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486c5363be4c09b70896b0b3db97db56de5f1226ca63de5ab425ff9453c4e46`

```dockerfile
```

-	Layers:
	-	`sha256:788a52ad55210bd2d4ed9fbbd6a152ba7b14dc3b7ee4c53d0f3a5cdedddf22d2`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:556db6b0e9df61bc612f019a8d4f6b5893969e89ddef9a58ffda03de01db0986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137322880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80105514d7c10daa8dcca6c73d62d0fcfcff8aef05f53027ed8f5b1e79221ea2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cbf04f008d9ef02dc799e294f7dfb15a6e1a7aa998c3ebd1abf85624fd8a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 7.4 MB (7437673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1a1cead3e82bc31db9d8227c36601c068da1b29538ac729dc38b62a255fa5`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73fe5fd8d6e91b61f554e5f4b6b205576d456d3ff11c7c7ae9f52c5dcbcb470`  
		Last Modified: Wed, 08 Oct 2025 20:23:28 GMT  
		Size: 18.4 MB (18402565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903fc967e46d7ed98ec9852c40659425d0fb55abfe4f3114b15a6d051a4c554f`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd58177b493833da3bb70027bbd00cd33ec2a6a6b37a4d8902ac62484e484b`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.4 MB (20352523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bada26e2a877a929758e22c849d20f156052c10b2613fc9122bf7b4e0d47050`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1b317dd5ec27fce62f574f1407e0d4893a1fe837e0e400de6dad22af04a1a`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35505dbf43402553e3b3c3b3c5f96a72c4772064bb797056463d77c9ced603d6`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cdb6aaff8e793882f2f2c50f51ed0c543232f7ab61ec1a55f57a7fff20e9fd`  
		Last Modified: Wed, 08 Oct 2025 20:54:16 GMT  
		Size: 8.6 MB (8610534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565524eb45b33cca7682947b28d97afa084eef35709cac083c7154e7ee93cb0`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 86.4 KB (86414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9137482da6d642b27169cbfe86fc0512df0e52ca658835c1e4a3354f9bdc05`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8654f9a663a2d9b3e893f06fd452e75bae44e486b46bd0acbf041c75356cfc5`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.5 MB (58461578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882f3a2fa1333d7ac2956f36df7b2ef37b65a14f4cd5a4a740b0bd54d1984e4`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509993fdecc5bd3d307dd22ffb54af7aebf642e0155a25d6035c07102dd71f5`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2d13d67ca9ef63f5eae6bba37fa287fcd66f661a5ab7002efbc8cb272edf5e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49ceb1c2519c405e3dfb782a06e6b1843eafc37059e91f61f0dfb01d8e828b`

```dockerfile
```

-	Layers:
	-	`sha256:843f07fbd7ee6fd55be49dd57f9c2124b4545c2bfe2d8430d990874abce54d87`  
		Last Modified: Wed, 08 Oct 2025 23:07:39 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9449b06cd22f308c6da3438072219d67a8f97108a97592e085569dae2ccdfc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139518141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fb75ea8a70cd3e982f7092098519a9358044c47278398e2b0e6584159ff182`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb8af46f57d19a7eff37ee20d0f745f2b25c2db3b03f886c5a262a2f978a5e`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 8.2 MB (8227626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e992b003cff6ac506b5770b58db53b0f264a7863c746e93a526eda5371cbb67`  
		Last Modified: Wed, 08 Oct 2025 20:25:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad120ba60793ead7541cf11a93928a23a8096c556b455d71e627b4770101eaf`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.2 MB (19232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bffd5eefa70b71759fe0ba576c4e5a833cd108f5798c6b7a09fe803268b02a`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e293265a4a953b06a80ea42dcf65f5105661e35dcd4e3db9929129fcbaef9`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec633ce7cb5252722f81f70be756b95d7ece1d440cd03c2b8e47cc8e81c6f3`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebf8988ea011982152e9840872446a584f00fba937e96bcbeb387ad10c2aca`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34003f92833935910091b03a75c728b9d21498e4db1400fd148a1efe0657544b`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f803108a8d61186171f4e10fe37dc2d290ac0b06ea7697d287f65327d18754fe`  
		Last Modified: Wed, 08 Oct 2025 20:33:22 GMT  
		Size: 10.0 MB (10032583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf713f8b6955fe83fa08d31cd4c30540fd734f00883ec9c827b12637f1baddd`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 99.5 KB (99542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9df8ad4f1ac1a4a2e84cf23938b4fc4a9d2aa2cdf2f3a0ef3611e36bb5f90c`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe98abb3a4ed4d7df089ae860cee02629c5ad7d91820952b15b2965d109ee2`  
		Last Modified: Wed, 08 Oct 2025 20:33:26 GMT  
		Size: 57.8 MB (57758061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241f05e886b9dc02131bb575c75a464cd577a7a7e082f41993e2180d95dc367`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fff9ec4efe80e48bed7b9607d6734de8054195e33b010de9d037f452d0a03d`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 3.3 KB (3292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b8efda5d1a7b765ec59ee503923e04d468f4202d8e4bd77ad5acc8ece82bfa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691659727245be56f7f4184be548de4c6f5841acc17ac30efe2d295503f06208`

```dockerfile
```

-	Layers:
	-	`sha256:1ea5e87c40e396c7f276887066b70aa11aa4cfabe79495c6ab35d902bb65a04b`  
		Last Modified: Wed, 08 Oct 2025 23:07:42 GMT  
		Size: 34.8 KB (34831 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-dind-alpine3.22`

```console
$ docker pull docker@sha256:7c3953162b1feca2aeb68a88ccb206485ff8c06177352ed9ffb3606354837869
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

### `docker:28.5.1-dind-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:17dd9c4154d3ca889b5b31e3e4b2818645819996f456e6c3e17b581737a44640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148653816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6219f96c48a526ca01fa59e2eca65ec67cd3f979f6c48dedeb14e6697dc42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0774022190f2b752e87a84c66b9a6ff1b3bbae43c893a860bd9a3fcbc4290ca`  
		Last Modified: Wed, 08 Oct 2025 20:34:07 GMT  
		Size: 9.5 MB (9507816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a691ee9764b4b3f4d9affb8c29ffc03f4c4d989298e2b2bfb93f4331b46f7`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a961a73cdd2322e8f59b2d11b5b5f03c41e6e488e12cb58d8a99bd02721ba90`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eaed86521d704b815068678197393163d0e1dc0dacde55392442b31b2bd192`  
		Last Modified: Wed, 08 Oct 2025 20:34:13 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49f61d997913f33514036426a2065cebcfafe63fa9d6464806bab8cff14914`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4b3e1409309a4af29d18da4edc4d1e06493028905509bce28eab52f2830e2`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:83e9d11602839d96665359ff81acf502ca43128754c722e7e02d5485220c97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ebaedf942d951b446ca1d48457cc7c468773b27f124b9f82e2761ec02af24`

```dockerfile
```

-	Layers:
	-	`sha256:60b958c4eb2101a33fd57b379ecb3eaddf7b960fa6558ae1e09fc807a11af41b`  
		Last Modified: Wed, 08 Oct 2025 23:07:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:23a94b59cfc54fb3f0a85562f77e1976ae427b6702eda1a6cc05665877ea7b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139351050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ad2dd9699bda1ab2c7d47dae8a76a2b693177a5f21a4d6ce52b8b5d54dc3f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7287652ad0f7417ae457a402f40a248670eddecae812df05328d7506b4eb7e`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 8.1 MB (8113337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431c8dbca316340be018038caec6bbb46de520002d7da495df2f3e22849718e`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2563734e87d4a41e756c5736d441c0d579cf5894976488bda29c158ca7b63c`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 18.4 MB (18418117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a98f22f147edc4650160e65326ae9aba04a825e888134bed99a30de9924eec`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e91a5ae2992f9361c096f7b969cbecfda20fe4c12e9c334d78dd56773286d8`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.4 MB (20371581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a13a1e08f9cd1e0584b24d8da93cf0b6f5047eeaf877caab0f4e47c1995081`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ecb3b6457a07ed0380f10034b6b0c3debcedce2a293f27f758b11cea20773f`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfb0083d4b0f462cdd77af85a4fc4fa2a17d49e30ec95f875998c1f8e27c759`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f97c4423935104b21120f03a4a4115af7e34c6549f33ba3f728f62acd6d3f8`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 9.5 MB (9461590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f59d52b9ff498c398252d10538d93ccda3c0928772008c1888f81cb9d58194f`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 90.0 KB (89976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555d288334111b4ea28df2e84d6e78b4a9351fef638dc5b83b1627892ede34c`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de61bedb5fac1b2191c9f3ab0f3dffca84f002acff72b937d528ff96cbf4d14`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.6 MB (58629069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e881d9a90366a6825183c33b18cb2464e9c0ba0ecb7195e91e15ab09201a7`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a5c01ee4ee6468b4679313e14ac47b9ae9211a3a82b2c619a88f3d050eda0a`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6e1b8fdc4984c0332556dbbf675047c01e0dc730a44ba6a1d254bc3bfb80e104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486c5363be4c09b70896b0b3db97db56de5f1226ca63de5ab425ff9453c4e46`

```dockerfile
```

-	Layers:
	-	`sha256:788a52ad55210bd2d4ed9fbbd6a152ba7b14dc3b7ee4c53d0f3a5cdedddf22d2`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:556db6b0e9df61bc612f019a8d4f6b5893969e89ddef9a58ffda03de01db0986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137322880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80105514d7c10daa8dcca6c73d62d0fcfcff8aef05f53027ed8f5b1e79221ea2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cbf04f008d9ef02dc799e294f7dfb15a6e1a7aa998c3ebd1abf85624fd8a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 7.4 MB (7437673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1a1cead3e82bc31db9d8227c36601c068da1b29538ac729dc38b62a255fa5`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73fe5fd8d6e91b61f554e5f4b6b205576d456d3ff11c7c7ae9f52c5dcbcb470`  
		Last Modified: Wed, 08 Oct 2025 20:23:28 GMT  
		Size: 18.4 MB (18402565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903fc967e46d7ed98ec9852c40659425d0fb55abfe4f3114b15a6d051a4c554f`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd58177b493833da3bb70027bbd00cd33ec2a6a6b37a4d8902ac62484e484b`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.4 MB (20352523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bada26e2a877a929758e22c849d20f156052c10b2613fc9122bf7b4e0d47050`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1b317dd5ec27fce62f574f1407e0d4893a1fe837e0e400de6dad22af04a1a`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35505dbf43402553e3b3c3b3c5f96a72c4772064bb797056463d77c9ced603d6`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cdb6aaff8e793882f2f2c50f51ed0c543232f7ab61ec1a55f57a7fff20e9fd`  
		Last Modified: Wed, 08 Oct 2025 20:54:16 GMT  
		Size: 8.6 MB (8610534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565524eb45b33cca7682947b28d97afa084eef35709cac083c7154e7ee93cb0`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 86.4 KB (86414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9137482da6d642b27169cbfe86fc0512df0e52ca658835c1e4a3354f9bdc05`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8654f9a663a2d9b3e893f06fd452e75bae44e486b46bd0acbf041c75356cfc5`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.5 MB (58461578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882f3a2fa1333d7ac2956f36df7b2ef37b65a14f4cd5a4a740b0bd54d1984e4`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509993fdecc5bd3d307dd22ffb54af7aebf642e0155a25d6035c07102dd71f5`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:2d13d67ca9ef63f5eae6bba37fa287fcd66f661a5ab7002efbc8cb272edf5e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49ceb1c2519c405e3dfb782a06e6b1843eafc37059e91f61f0dfb01d8e828b`

```dockerfile
```

-	Layers:
	-	`sha256:843f07fbd7ee6fd55be49dd57f9c2124b4545c2bfe2d8430d990874abce54d87`  
		Last Modified: Wed, 08 Oct 2025 23:07:39 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9449b06cd22f308c6da3438072219d67a8f97108a97592e085569dae2ccdfc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139518141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fb75ea8a70cd3e982f7092098519a9358044c47278398e2b0e6584159ff182`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb8af46f57d19a7eff37ee20d0f745f2b25c2db3b03f886c5a262a2f978a5e`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 8.2 MB (8227626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e992b003cff6ac506b5770b58db53b0f264a7863c746e93a526eda5371cbb67`  
		Last Modified: Wed, 08 Oct 2025 20:25:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad120ba60793ead7541cf11a93928a23a8096c556b455d71e627b4770101eaf`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.2 MB (19232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bffd5eefa70b71759fe0ba576c4e5a833cd108f5798c6b7a09fe803268b02a`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e293265a4a953b06a80ea42dcf65f5105661e35dcd4e3db9929129fcbaef9`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec633ce7cb5252722f81f70be756b95d7ece1d440cd03c2b8e47cc8e81c6f3`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebf8988ea011982152e9840872446a584f00fba937e96bcbeb387ad10c2aca`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34003f92833935910091b03a75c728b9d21498e4db1400fd148a1efe0657544b`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f803108a8d61186171f4e10fe37dc2d290ac0b06ea7697d287f65327d18754fe`  
		Last Modified: Wed, 08 Oct 2025 20:33:22 GMT  
		Size: 10.0 MB (10032583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf713f8b6955fe83fa08d31cd4c30540fd734f00883ec9c827b12637f1baddd`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 99.5 KB (99542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9df8ad4f1ac1a4a2e84cf23938b4fc4a9d2aa2cdf2f3a0ef3611e36bb5f90c`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe98abb3a4ed4d7df089ae860cee02629c5ad7d91820952b15b2965d109ee2`  
		Last Modified: Wed, 08 Oct 2025 20:33:26 GMT  
		Size: 57.8 MB (57758061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241f05e886b9dc02131bb575c75a464cd577a7a7e082f41993e2180d95dc367`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fff9ec4efe80e48bed7b9607d6734de8054195e33b010de9d037f452d0a03d`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 3.3 KB (3292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:b8efda5d1a7b765ec59ee503923e04d468f4202d8e4bd77ad5acc8ece82bfa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691659727245be56f7f4184be548de4c6f5841acc17ac30efe2d295503f06208`

```dockerfile
```

-	Layers:
	-	`sha256:1ea5e87c40e396c7f276887066b70aa11aa4cfabe79495c6ab35d902bb65a04b`  
		Last Modified: Wed, 08 Oct 2025 23:07:42 GMT  
		Size: 34.8 KB (34831 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:28.5.1-windowsservercore`

```console
$ docker pull docker@sha256:337c819e1e92bbe665964fa9ff8420a91cd889d8b99ba336749af5eb20bd5502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5.1-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.5.1-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:08fcf22b324f01b24d7d6c9edb2a077743fcb7a420e4263f0b1bca4952e41c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a850d0d3454900418bf8bd97acb002622a6ed5b1a77fa6fd76412b1f4f8ef768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:28.5.1-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:19b6a32c14b2d71c0ef4575f6ad1712dca6f23f73155a60bb07c0d1f4fb00418
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
$ docker pull docker@sha256:2ceaba2d9fe94568625978458a4f93e81b294fb96927fe2602b2cedd0bf9aea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76218700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6fa733b2ab715cbe441dd3c8359166d4973a32bd0dd734ee6ae29d4674c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f0a7b75fac3ac0bdc9c259b3dee99d1b76ee443dac8cfba8dd29f35c802a2c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faabc0adf6d1af8f9982e75c4aa3764cfb09e6b1e25ea0d359271125a065cdf`

```dockerfile
```

-	Layers:
	-	`sha256:c9a093a89c86df61de202e883b8edc52d7bda13f8a30db29a33e6bb0cd17fb1e`  
		Last Modified: Wed, 08 Oct 2025 23:07:49 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ee987cd4ffdfcf157a4df2756fe649bcf28040e3120405621f2106d5b95a65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71167610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8797fa6025da5f6cf43e5c7d5a861a13c1310981b47c73deaf111403fc763d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:913a776a1640e30a4787299519798eece3065c0a11f093478d4fd2729f8d09f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb92b7516dfaf1ff47deaa4c43d8c5da5e5d5a3063009bcbfaca11b0f4638e`

```dockerfile
```

-	Layers:
	-	`sha256:c6429b41ec7e43b858d6fc47cfbdf63b75084dd78f7a456a4109e8ef5fa7d9ae`  
		Last Modified: Wed, 08 Oct 2025 23:07:52 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ca49543195a1e53642ae43f301269504f6157911c85df2e1fe9a48f2b641a5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70160704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3864f57cedbc27d92173d6ce1ff98bd62deb24f2f012baa9bfd8c86bd18a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:27cfbd43240b2a36d9206e8d65ffa68cc828cc333dee94860ea8fe50fcdedc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54f87f9a325c1a28f3911b733bb8d436d5a344e5f4cab025423060c3122f12`

```dockerfile
```

-	Layers:
	-	`sha256:1c73b917de5769ed1585050836dd77eb606db44134e96525d7b6be3ce44aa0d5`  
		Last Modified: Wed, 08 Oct 2025 23:07:56 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a246a4a6c87424fc8e26fbd5f8f26e1ac19e2745da7e3c40be18b8c265ae1bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71629206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9625f7aa2680d221b2ee306d6dd46be38d361c45cde6e47d84115ebc8faa619c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b2a82343ac247cca758d9a1cf13ec29c7705a3d4f11eac33840976a005f375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcf6dab5064a1fd34f33a9e7a5856d82a8f5ae4eb063493a494c9439eda61ad`

```dockerfile
```

-	Layers:
	-	`sha256:7879f0a2aa84744862fb9b29e3a5a4bcf9495ec25822e20b5e68e59056b15992`  
		Last Modified: Wed, 08 Oct 2025 23:07:59 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:7c3953162b1feca2aeb68a88ccb206485ff8c06177352ed9ffb3606354837869
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
$ docker pull docker@sha256:17dd9c4154d3ca889b5b31e3e4b2818645819996f456e6c3e17b581737a44640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148653816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6219f96c48a526ca01fa59e2eca65ec67cd3f979f6c48dedeb14e6697dc42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0774022190f2b752e87a84c66b9a6ff1b3bbae43c893a860bd9a3fcbc4290ca`  
		Last Modified: Wed, 08 Oct 2025 20:34:07 GMT  
		Size: 9.5 MB (9507816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a691ee9764b4b3f4d9affb8c29ffc03f4c4d989298e2b2bfb93f4331b46f7`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a961a73cdd2322e8f59b2d11b5b5f03c41e6e488e12cb58d8a99bd02721ba90`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eaed86521d704b815068678197393163d0e1dc0dacde55392442b31b2bd192`  
		Last Modified: Wed, 08 Oct 2025 20:34:13 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49f61d997913f33514036426a2065cebcfafe63fa9d6464806bab8cff14914`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4b3e1409309a4af29d18da4edc4d1e06493028905509bce28eab52f2830e2`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:83e9d11602839d96665359ff81acf502ca43128754c722e7e02d5485220c97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ebaedf942d951b446ca1d48457cc7c468773b27f124b9f82e2761ec02af24`

```dockerfile
```

-	Layers:
	-	`sha256:60b958c4eb2101a33fd57b379ecb3eaddf7b960fa6558ae1e09fc807a11af41b`  
		Last Modified: Wed, 08 Oct 2025 23:07:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:23a94b59cfc54fb3f0a85562f77e1976ae427b6702eda1a6cc05665877ea7b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139351050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ad2dd9699bda1ab2c7d47dae8a76a2b693177a5f21a4d6ce52b8b5d54dc3f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7287652ad0f7417ae457a402f40a248670eddecae812df05328d7506b4eb7e`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 8.1 MB (8113337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431c8dbca316340be018038caec6bbb46de520002d7da495df2f3e22849718e`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2563734e87d4a41e756c5736d441c0d579cf5894976488bda29c158ca7b63c`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 18.4 MB (18418117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a98f22f147edc4650160e65326ae9aba04a825e888134bed99a30de9924eec`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e91a5ae2992f9361c096f7b969cbecfda20fe4c12e9c334d78dd56773286d8`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.4 MB (20371581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a13a1e08f9cd1e0584b24d8da93cf0b6f5047eeaf877caab0f4e47c1995081`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ecb3b6457a07ed0380f10034b6b0c3debcedce2a293f27f758b11cea20773f`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfb0083d4b0f462cdd77af85a4fc4fa2a17d49e30ec95f875998c1f8e27c759`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f97c4423935104b21120f03a4a4115af7e34c6549f33ba3f728f62acd6d3f8`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 9.5 MB (9461590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f59d52b9ff498c398252d10538d93ccda3c0928772008c1888f81cb9d58194f`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 90.0 KB (89976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555d288334111b4ea28df2e84d6e78b4a9351fef638dc5b83b1627892ede34c`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de61bedb5fac1b2191c9f3ab0f3dffca84f002acff72b937d528ff96cbf4d14`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.6 MB (58629069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e881d9a90366a6825183c33b18cb2464e9c0ba0ecb7195e91e15ab09201a7`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a5c01ee4ee6468b4679313e14ac47b9ae9211a3a82b2c619a88f3d050eda0a`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:6e1b8fdc4984c0332556dbbf675047c01e0dc730a44ba6a1d254bc3bfb80e104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486c5363be4c09b70896b0b3db97db56de5f1226ca63de5ab425ff9453c4e46`

```dockerfile
```

-	Layers:
	-	`sha256:788a52ad55210bd2d4ed9fbbd6a152ba7b14dc3b7ee4c53d0f3a5cdedddf22d2`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:556db6b0e9df61bc612f019a8d4f6b5893969e89ddef9a58ffda03de01db0986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137322880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80105514d7c10daa8dcca6c73d62d0fcfcff8aef05f53027ed8f5b1e79221ea2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cbf04f008d9ef02dc799e294f7dfb15a6e1a7aa998c3ebd1abf85624fd8a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 7.4 MB (7437673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1a1cead3e82bc31db9d8227c36601c068da1b29538ac729dc38b62a255fa5`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73fe5fd8d6e91b61f554e5f4b6b205576d456d3ff11c7c7ae9f52c5dcbcb470`  
		Last Modified: Wed, 08 Oct 2025 20:23:28 GMT  
		Size: 18.4 MB (18402565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903fc967e46d7ed98ec9852c40659425d0fb55abfe4f3114b15a6d051a4c554f`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd58177b493833da3bb70027bbd00cd33ec2a6a6b37a4d8902ac62484e484b`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.4 MB (20352523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bada26e2a877a929758e22c849d20f156052c10b2613fc9122bf7b4e0d47050`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1b317dd5ec27fce62f574f1407e0d4893a1fe837e0e400de6dad22af04a1a`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35505dbf43402553e3b3c3b3c5f96a72c4772064bb797056463d77c9ced603d6`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cdb6aaff8e793882f2f2c50f51ed0c543232f7ab61ec1a55f57a7fff20e9fd`  
		Last Modified: Wed, 08 Oct 2025 20:54:16 GMT  
		Size: 8.6 MB (8610534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565524eb45b33cca7682947b28d97afa084eef35709cac083c7154e7ee93cb0`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 86.4 KB (86414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9137482da6d642b27169cbfe86fc0512df0e52ca658835c1e4a3354f9bdc05`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8654f9a663a2d9b3e893f06fd452e75bae44e486b46bd0acbf041c75356cfc5`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.5 MB (58461578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882f3a2fa1333d7ac2956f36df7b2ef37b65a14f4cd5a4a740b0bd54d1984e4`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509993fdecc5bd3d307dd22ffb54af7aebf642e0155a25d6035c07102dd71f5`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:2d13d67ca9ef63f5eae6bba37fa287fcd66f661a5ab7002efbc8cb272edf5e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49ceb1c2519c405e3dfb782a06e6b1843eafc37059e91f61f0dfb01d8e828b`

```dockerfile
```

-	Layers:
	-	`sha256:843f07fbd7ee6fd55be49dd57f9c2124b4545c2bfe2d8430d990874abce54d87`  
		Last Modified: Wed, 08 Oct 2025 23:07:39 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9449b06cd22f308c6da3438072219d67a8f97108a97592e085569dae2ccdfc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139518141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fb75ea8a70cd3e982f7092098519a9358044c47278398e2b0e6584159ff182`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb8af46f57d19a7eff37ee20d0f745f2b25c2db3b03f886c5a262a2f978a5e`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 8.2 MB (8227626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e992b003cff6ac506b5770b58db53b0f264a7863c746e93a526eda5371cbb67`  
		Last Modified: Wed, 08 Oct 2025 20:25:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad120ba60793ead7541cf11a93928a23a8096c556b455d71e627b4770101eaf`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.2 MB (19232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bffd5eefa70b71759fe0ba576c4e5a833cd108f5798c6b7a09fe803268b02a`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e293265a4a953b06a80ea42dcf65f5105661e35dcd4e3db9929129fcbaef9`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec633ce7cb5252722f81f70be756b95d7ece1d440cd03c2b8e47cc8e81c6f3`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebf8988ea011982152e9840872446a584f00fba937e96bcbeb387ad10c2aca`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34003f92833935910091b03a75c728b9d21498e4db1400fd148a1efe0657544b`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f803108a8d61186171f4e10fe37dc2d290ac0b06ea7697d287f65327d18754fe`  
		Last Modified: Wed, 08 Oct 2025 20:33:22 GMT  
		Size: 10.0 MB (10032583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf713f8b6955fe83fa08d31cd4c30540fd734f00883ec9c827b12637f1baddd`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 99.5 KB (99542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9df8ad4f1ac1a4a2e84cf23938b4fc4a9d2aa2cdf2f3a0ef3611e36bb5f90c`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe98abb3a4ed4d7df089ae860cee02629c5ad7d91820952b15b2965d109ee2`  
		Last Modified: Wed, 08 Oct 2025 20:33:26 GMT  
		Size: 57.8 MB (57758061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241f05e886b9dc02131bb575c75a464cd577a7a7e082f41993e2180d95dc367`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fff9ec4efe80e48bed7b9607d6734de8054195e33b010de9d037f452d0a03d`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 3.3 KB (3292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b8efda5d1a7b765ec59ee503923e04d468f4202d8e4bd77ad5acc8ece82bfa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691659727245be56f7f4184be548de4c6f5841acc17ac30efe2d295503f06208`

```dockerfile
```

-	Layers:
	-	`sha256:1ea5e87c40e396c7f276887066b70aa11aa4cfabe79495c6ab35d902bb65a04b`  
		Last Modified: Wed, 08 Oct 2025 23:07:42 GMT  
		Size: 34.8 KB (34831 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:eeb43ad630a5165c910f03041a590147ddb1c2632be3a3c397e9b2c2b4efa7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:b3d53c924e34d7e003f601d8d6222844b9c1b71b7aa0b2ed4655a6b30fe32602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169675916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78479fdc55be9d0c2772a94ab8b66e905f686b58a754da0f12cd11b4ba460167`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD []
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f4121261305cd808f866e5cc468c62c7b691048458ce84c73cebc8744a0f5c`  
		Last Modified: Fri, 03 Oct 2025 15:42:57 GMT  
		Size: 8.2 MB (8206013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacb763c34fa98faf157ad30ac845055c7e17d6bc356a735dd34979b2ca3dcd`  
		Last Modified: Fri, 03 Oct 2025 15:42:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82baaa61b0bd5e833b9bf0dce2a5ba042e651d1dae98dcecd76a54d85245f705`  
		Last Modified: Fri, 03 Oct 2025 15:43:00 GMT  
		Size: 20.4 MB (20429721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c233148e55acfe21ab7559acf33645c62cab15c2786fb755b117d0f761692214`  
		Last Modified: Fri, 03 Oct 2025 15:43:04 GMT  
		Size: 22.2 MB (22158310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a01365128829f855670516e240e079aaa07cca78da2106a03fe8cc88723c3c6`  
		Last Modified: Fri, 03 Oct 2025 15:43:10 GMT  
		Size: 21.7 MB (21656766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d97b7b769f0ef0ffff5fb8721b8852aab640d625cccad858457c7ccdc01909`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252ca38c80c99c59f88eb9177337a5d1e1be51a71bca74077ce10d0e2db2ff6`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f710bb1cc914e30eac705c8d79e2b6fac559197d538c0a843bfdd992a69bfe1`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bd32a0ea96da36ee694f909a448f72d9ce8f3161366150204ce43f92f3ef25`  
		Last Modified: Fri, 03 Oct 2025 16:55:35 GMT  
		Size: 9.5 MB (9507812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b78db0b14600437995bb4b41a16d542cc1c29e47d131a154fcd0e71e1240e7`  
		Last Modified: Fri, 03 Oct 2025 16:33:46 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02844b1b965c7106b174fa8fcc81da5932ae550f52b2cdea2f4b1cbc72cf9103`  
		Last Modified: Fri, 03 Oct 2025 16:33:51 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c0d4f3fc3deda7540f99bf89eb4616d8fe2bf6fde04101d3c62817b55b32ed`  
		Last Modified: Fri, 03 Oct 2025 16:55:36 GMT  
		Size: 62.8 MB (62827332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2b4197469badf8d75becb38e327e689d7b466f9a06cbf2e22c1574489684fc`  
		Last Modified: Fri, 03 Oct 2025 16:33:54 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733f9fcc3eeee9d72d8b472b1225e3228f39f1cefe71d8dff9f1a2c710decce`  
		Last Modified: Fri, 03 Oct 2025 16:33:57 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac14d1bbef2a00ee6148a84da6d122959f4469478e896e6b0238d37228c12e58`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 3.4 MB (3398331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a4cba6aa490126672884ec1cc7fc81c87c39f7a7b752a3a27031de81cc7e66`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3068b13530be21c371198cff4b2617ff2f7bf794a5ff5f9daf01addd778aa4b0`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aed80e8577ba3b89d9e8425fc00a705532e626ca3fc051bad538409c0399762`  
		Last Modified: Fri, 03 Oct 2025 16:56:14 GMT  
		Size: 17.6 MB (17592032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069ff56a1905eb0680d22ee4587a1a1ba638f709814aca49b750b3c4bf3531f6`  
		Last Modified: Fri, 03 Oct 2025 16:56:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:93a89793da5adcc19ef3c9827d45c6ecb2767c1a1585dc874a34e2e3565f084f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119379607dbb4d2e6842aa149d585b6259e03e4b136a8b29a877d1fd94e7a05f`

```dockerfile
```

-	Layers:
	-	`sha256:91562a8e6c08e44f1300395f13fbf8c2f9e8521ccc3a5a2685e8553f477b409e`  
		Last Modified: Fri, 03 Oct 2025 17:07:59 GMT  
		Size: 30.6 KB (30636 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:96a3c2358a11eb6c0b8b8697af03c763b040a4289d5cdb41afce7cccfdc6a7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160960944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09fc28f780b87f424eac4f8d8e1a3e2f8b076509e298aa9f1c3af3ce13c6945`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD []
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befee8c2b0ad40f8afec285692dd9de306244ab77849362b32f364598f4dd856`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 8.2 MB (8227655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81db965703fb492a9487f0707728f846ca5016cffbe4cca14a9aaedf3fe47be`  
		Last Modified: Fri, 03 Oct 2025 16:10:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae023da43925318e9d906c7752c90968e4e76401eff1a13c13a02dfad260775`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 19.2 MB (19238158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d084ed095dcaaa56e75d1464d58172ca160961091fd6c2110b81301c1c8d144a`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 20.3 MB (20274240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5cbf3334db63fb72ebb37340a3158221d6151607e4b01c5be6b44f4c2a1f35`  
		Last Modified: Fri, 03 Oct 2025 16:10:10 GMT  
		Size: 19.8 MB (19779981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a37c322750556c7e8922a42c05e513ce640dbe5059b406843b4285c15f28be`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ee98d68b79d3a825b7c3d7d4492c505cae7e7ee829b8da41259b5372f704be`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06880fc24b1d74868cf537077a0bd0cc09b9cb315d6f2e5ba9ae3fe57405085f`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e663db0fdfaf3e5f40f7c3d7c3d51cfa62bbe43ddfcb4fe99cb8b6c637f6aa`  
		Last Modified: Fri, 03 Oct 2025 16:11:02 GMT  
		Size: 10.0 MB (10032639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5e31e2508033fa71a6e9c996b28c63fb8717b1fb04950cc9bf8ab9c496715c`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 99.6 KB (99551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44d97f98752505c225f3d7bf9a163d9522bb8c15f839dde10ca592bec612151`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db3a1adaf72d283f41dd82a794dd8a21401cf97b9547986d552142a747eb5ae`  
		Last Modified: Fri, 03 Oct 2025 16:11:06 GMT  
		Size: 57.8 MB (57759208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0ea7e65ba6a9a348e2c362f6ee2128c9cbbc4fe766157fac25a52324ef2e0c`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8003cd90da085be86d46c270b3ffed416d670d6fb46dc211845eaad27c21794`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210fc14d10dd6889f85a6c0dda51131547e11a4b09c342a41f267e3b05025bb`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 3.4 MB (3389873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650ea26cdb1e4676d6bce162d7e5a937b93e2705cc86380b54dd03d1e8b1abd3`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5728e12ff2b23e1c18b5c20970862362841a7011baa80aef4a45d5a1b108115`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30951d5b864c3c60fe2adf5433ff9e1d915fc52fdd40fae1766a1948ac8ef345`  
		Last Modified: Fri, 03 Oct 2025 17:08:19 GMT  
		Size: 18.0 MB (18019399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056d88955c46abf8014f4e3163803203a97c96513ab2783aee987fd1cc078700`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4025f450b00c6226d6682f17fbdaa8ff0aca575e36b82377be3680a70b1008ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd180d64e35b20ae847a8335cd5554d37b68ed547c4530d96e617dd92f1a9a0`

```dockerfile
```

-	Layers:
	-	`sha256:e94643b935420367d72f27be406ef5a64f8862ab497d1cb7c6291454821ec49c`  
		Last Modified: Fri, 03 Oct 2025 17:08:03 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:7c3953162b1feca2aeb68a88ccb206485ff8c06177352ed9ffb3606354837869
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
$ docker pull docker@sha256:17dd9c4154d3ca889b5b31e3e4b2818645819996f456e6c3e17b581737a44640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148653816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6219f96c48a526ca01fa59e2eca65ec67cd3f979f6c48dedeb14e6697dc42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed298f4ad7e4c47a1c735f4a3412576347fbaf48fa0976f6335b9707fa0b3866`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 8.2 MB (8205983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf26d7ac7ab58218a011f55daff4a712a7a9cfa9851c5f65d2526febf2fe6a`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f2f1cd950ffc54f8f59a799825d5a2671303221070ba721e050ed66393c0`  
		Last Modified: Wed, 08 Oct 2025 20:23:09 GMT  
		Size: 20.4 MB (20426223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4cb4035ab0510556fd5e15a8703130f010f26e2e97b216fad057bf6ec5a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 22.2 MB (22158450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf31be1ecc55cb07335b48f6392a638fb6d1657090c4b4c5e7f82b342b9cf20`  
		Last Modified: Wed, 08 Oct 2025 20:23:10 GMT  
		Size: 21.6 MB (21626203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335a4de0370c88ce6f5a6b3ec15deede1023caa20615ca5741c905d42b949cc`  
		Last Modified: Wed, 08 Oct 2025 20:23:07 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118fee909edbace9386f9cad6f30651153502b6c13040e18bfe965f4018068f`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98ffb60b067888429cc3444b9d903ceae66bd097fdfb1da3e53db83f3da376`  
		Last Modified: Wed, 08 Oct 2025 20:23:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0774022190f2b752e87a84c66b9a6ff1b3bbae43c893a860bd9a3fcbc4290ca`  
		Last Modified: Wed, 08 Oct 2025 20:34:07 GMT  
		Size: 9.5 MB (9507816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a691ee9764b4b3f4d9affb8c29ffc03f4c4d989298e2b2bfb93f4331b46f7`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a961a73cdd2322e8f59b2d11b5b5f03c41e6e488e12cb58d8a99bd02721ba90`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eaed86521d704b815068678197393163d0e1dc0dacde55392442b31b2bd192`  
		Last Modified: Wed, 08 Oct 2025 20:34:13 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49f61d997913f33514036426a2065cebcfafe63fa9d6464806bab8cff14914`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4b3e1409309a4af29d18da4edc4d1e06493028905509bce28eab52f2830e2`  
		Last Modified: Wed, 08 Oct 2025 20:34:05 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:83e9d11602839d96665359ff81acf502ca43128754c722e7e02d5485220c97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ebaedf942d951b446ca1d48457cc7c468773b27f124b9f82e2761ec02af24`

```dockerfile
```

-	Layers:
	-	`sha256:60b958c4eb2101a33fd57b379ecb3eaddf7b960fa6558ae1e09fc807a11af41b`  
		Last Modified: Wed, 08 Oct 2025 23:07:33 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:23a94b59cfc54fb3f0a85562f77e1976ae427b6702eda1a6cc05665877ea7b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139351050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ad2dd9699bda1ab2c7d47dae8a76a2b693177a5f21a4d6ce52b8b5d54dc3f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7287652ad0f7417ae457a402f40a248670eddecae812df05328d7506b4eb7e`  
		Last Modified: Wed, 08 Oct 2025 20:23:12 GMT  
		Size: 8.1 MB (8113337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431c8dbca316340be018038caec6bbb46de520002d7da495df2f3e22849718e`  
		Last Modified: Wed, 08 Oct 2025 20:23:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2563734e87d4a41e756c5736d441c0d579cf5894976488bda29c158ca7b63c`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 18.4 MB (18418117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a98f22f147edc4650160e65326ae9aba04a825e888134bed99a30de9924eec`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e91a5ae2992f9361c096f7b969cbecfda20fe4c12e9c334d78dd56773286d8`  
		Last Modified: Wed, 08 Oct 2025 20:23:14 GMT  
		Size: 20.4 MB (20371581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a13a1e08f9cd1e0584b24d8da93cf0b6f5047eeaf877caab0f4e47c1995081`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ecb3b6457a07ed0380f10034b6b0c3debcedce2a293f27f758b11cea20773f`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfb0083d4b0f462cdd77af85a4fc4fa2a17d49e30ec95f875998c1f8e27c759`  
		Last Modified: Wed, 08 Oct 2025 20:23:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f97c4423935104b21120f03a4a4115af7e34c6549f33ba3f728f62acd6d3f8`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 9.5 MB (9461590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f59d52b9ff498c398252d10538d93ccda3c0928772008c1888f81cb9d58194f`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 90.0 KB (89976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555d288334111b4ea28df2e84d6e78b4a9351fef638dc5b83b1627892ede34c`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de61bedb5fac1b2191c9f3ab0f3dffca84f002acff72b937d528ff96cbf4d14`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.6 MB (58629069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e881d9a90366a6825183c33b18cb2464e9c0ba0ecb7195e91e15ab09201a7`  
		Last Modified: Wed, 08 Oct 2025 20:33:07 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a5c01ee4ee6468b4679313e14ac47b9ae9211a3a82b2c619a88f3d050eda0a`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:6e1b8fdc4984c0332556dbbf675047c01e0dc730a44ba6a1d254bc3bfb80e104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486c5363be4c09b70896b0b3db97db56de5f1226ca63de5ab425ff9453c4e46`

```dockerfile
```

-	Layers:
	-	`sha256:788a52ad55210bd2d4ed9fbbd6a152ba7b14dc3b7ee4c53d0f3a5cdedddf22d2`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:556db6b0e9df61bc612f019a8d4f6b5893969e89ddef9a58ffda03de01db0986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137322880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80105514d7c10daa8dcca6c73d62d0fcfcff8aef05f53027ed8f5b1e79221ea2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cbf04f008d9ef02dc799e294f7dfb15a6e1a7aa998c3ebd1abf85624fd8a5`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 7.4 MB (7437673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1a1cead3e82bc31db9d8227c36601c068da1b29538ac729dc38b62a255fa5`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73fe5fd8d6e91b61f554e5f4b6b205576d456d3ff11c7c7ae9f52c5dcbcb470`  
		Last Modified: Wed, 08 Oct 2025 20:23:28 GMT  
		Size: 18.4 MB (18402565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903fc967e46d7ed98ec9852c40659425d0fb55abfe4f3114b15a6d051a4c554f`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd58177b493833da3bb70027bbd00cd33ec2a6a6b37a4d8902ac62484e484b`  
		Last Modified: Wed, 08 Oct 2025 20:23:23 GMT  
		Size: 20.4 MB (20352523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bada26e2a877a929758e22c849d20f156052c10b2613fc9122bf7b4e0d47050`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1b317dd5ec27fce62f574f1407e0d4893a1fe837e0e400de6dad22af04a1a`  
		Last Modified: Wed, 08 Oct 2025 20:23:21 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35505dbf43402553e3b3c3b3c5f96a72c4772064bb797056463d77c9ced603d6`  
		Last Modified: Wed, 08 Oct 2025 20:23:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cdb6aaff8e793882f2f2c50f51ed0c543232f7ab61ec1a55f57a7fff20e9fd`  
		Last Modified: Wed, 08 Oct 2025 20:54:16 GMT  
		Size: 8.6 MB (8610534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565524eb45b33cca7682947b28d97afa084eef35709cac083c7154e7ee93cb0`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 86.4 KB (86414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9137482da6d642b27169cbfe86fc0512df0e52ca658835c1e4a3354f9bdc05`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8654f9a663a2d9b3e893f06fd452e75bae44e486b46bd0acbf041c75356cfc5`  
		Last Modified: Wed, 08 Oct 2025 20:33:13 GMT  
		Size: 58.5 MB (58461578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882f3a2fa1333d7ac2956f36df7b2ef37b65a14f4cd5a4a740b0bd54d1984e4`  
		Last Modified: Wed, 08 Oct 2025 20:33:06 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509993fdecc5bd3d307dd22ffb54af7aebf642e0155a25d6035c07102dd71f5`  
		Last Modified: Wed, 08 Oct 2025 20:33:05 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:2d13d67ca9ef63f5eae6bba37fa287fcd66f661a5ab7002efbc8cb272edf5e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49ceb1c2519c405e3dfb782a06e6b1843eafc37059e91f61f0dfb01d8e828b`

```dockerfile
```

-	Layers:
	-	`sha256:843f07fbd7ee6fd55be49dd57f9c2124b4545c2bfe2d8430d990874abce54d87`  
		Last Modified: Wed, 08 Oct 2025 23:07:39 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9449b06cd22f308c6da3438072219d67a8f97108a97592e085569dae2ccdfc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139518141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fb75ea8a70cd3e982f7092098519a9358044c47278398e2b0e6584159ff182`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb8af46f57d19a7eff37ee20d0f745f2b25c2db3b03f886c5a262a2f978a5e`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 8.2 MB (8227626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e992b003cff6ac506b5770b58db53b0f264a7863c746e93a526eda5371cbb67`  
		Last Modified: Wed, 08 Oct 2025 20:25:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad120ba60793ead7541cf11a93928a23a8096c556b455d71e627b4770101eaf`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.2 MB (19232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bffd5eefa70b71759fe0ba576c4e5a833cd108f5798c6b7a09fe803268b02a`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e293265a4a953b06a80ea42dcf65f5105661e35dcd4e3db9929129fcbaef9`  
		Last Modified: Wed, 08 Oct 2025 20:25:21 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec633ce7cb5252722f81f70be756b95d7ece1d440cd03c2b8e47cc8e81c6f3`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebf8988ea011982152e9840872446a584f00fba937e96bcbeb387ad10c2aca`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34003f92833935910091b03a75c728b9d21498e4db1400fd148a1efe0657544b`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f803108a8d61186171f4e10fe37dc2d290ac0b06ea7697d287f65327d18754fe`  
		Last Modified: Wed, 08 Oct 2025 20:33:22 GMT  
		Size: 10.0 MB (10032583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf713f8b6955fe83fa08d31cd4c30540fd734f00883ec9c827b12637f1baddd`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 99.5 KB (99542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9df8ad4f1ac1a4a2e84cf23938b4fc4a9d2aa2cdf2f3a0ef3611e36bb5f90c`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe98abb3a4ed4d7df089ae860cee02629c5ad7d91820952b15b2965d109ee2`  
		Last Modified: Wed, 08 Oct 2025 20:33:26 GMT  
		Size: 57.8 MB (57758061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241f05e886b9dc02131bb575c75a464cd577a7a7e082f41993e2180d95dc367`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fff9ec4efe80e48bed7b9607d6734de8054195e33b010de9d037f452d0a03d`  
		Last Modified: Wed, 08 Oct 2025 20:33:20 GMT  
		Size: 3.3 KB (3292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:b8efda5d1a7b765ec59ee503923e04d468f4202d8e4bd77ad5acc8ece82bfa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691659727245be56f7f4184be548de4c6f5841acc17ac30efe2d295503f06208`

```dockerfile
```

-	Layers:
	-	`sha256:1ea5e87c40e396c7f276887066b70aa11aa4cfabe79495c6ab35d902bb65a04b`  
		Last Modified: Wed, 08 Oct 2025 23:07:42 GMT  
		Size: 34.8 KB (34831 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:337c819e1e92bbe665964fa9ff8420a91cd889d8b99ba336749af5eb20bd5502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:08fcf22b324f01b24d7d6c9edb2a077743fcb7a420e4263f0b1bca4952e41c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a850d0d3454900418bf8bd97acb002622a6ed5b1a77fa6fd76412b1f4f8ef768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
