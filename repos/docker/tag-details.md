<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.0`](#docker290)
-	[`docker:29.0-cli`](#docker290-cli)
-	[`docker:29.0-dind`](#docker290-dind)
-	[`docker:29.0-dind-rootless`](#docker290-dind-rootless)
-	[`docker:29.0-windowsservercore`](#docker290-windowsservercore)
-	[`docker:29.0-windowsservercore-ltsc2022`](#docker290-windowsservercore-ltsc2022)
-	[`docker:29.0-windowsservercore-ltsc2025`](#docker290-windowsservercore-ltsc2025)
-	[`docker:29.0.0`](#docker2900)
-	[`docker:29.0.0-alpine3.22`](#docker2900-alpine322)
-	[`docker:29.0.0-cli`](#docker2900-cli)
-	[`docker:29.0.0-cli-alpine3.22`](#docker2900-cli-alpine322)
-	[`docker:29.0.0-dind`](#docker2900-dind)
-	[`docker:29.0.0-dind-alpine3.22`](#docker2900-dind-alpine322)
-	[`docker:29.0.0-dind-rootless`](#docker2900-dind-rootless)
-	[`docker:29.0.0-windowsservercore`](#docker2900-windowsservercore)
-	[`docker:29.0.0-windowsservercore-ltsc2022`](#docker2900-windowsservercore-ltsc2022)
-	[`docker:29.0.0-windowsservercore-ltsc2025`](#docker2900-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:96789d56621ae702a2f8aa316c87a1a1875dd3f02bf67cdcb56a524a09fa3af9
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
$ docker pull docker@sha256:df7efe7183e533112a8236c5fddb1edf12c96fb2feba3b6b693a285bd7bb993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143957895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cdce60b4d9596765151d2508cad4e3441223cf71e32ba68015def44b654c2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:bf82da9d97fb017eb52fe800bcb19e47f54474e8d981b8682beb615517afd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0164e514b2ea3e21ae8f8c5486cd2d19628d181877991e1232da20933c44b`

```dockerfile
```

-	Layers:
	-	`sha256:d474ac080071d8e06b197e991ae6cd69e0220b949c3e867e07644315c15c39d2`  
		Last Modified: Tue, 11 Nov 2025 06:07:32 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:801cd28b5bdd6f880f7551901af30f6f084bd70c09dffa4ca0d2cace1eba03af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135991944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c369e847de2b33daebebfd4b7581651530f43a5f1705341a2e0fd7e3f1090`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d9e03480f36684f99c499bcac854458fc59fbd5fa1590b2a75308769f18bf`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 7.2 MB (7230266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4413fdb49a4b4c681741a79c06d306c0adce974437e167ab302104c09817f74f`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 89.9 KB (89949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ef3e596708743d134b73dba182acb89d52baa28af431f822db748a0b6e68a7`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84002f98aaa912e73b1fefcb7d1eb964dde81fa74a2ecdb42592b3199151e4a`  
		Last Modified: Tue, 11 Nov 2025 02:10:03 GMT  
		Size: 58.2 MB (58226172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c833c392dc7ac6d8703b1d37c747c18bbb1a7b715d2310cb1714175f258eb28`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefbb114f52aff835ec78ec55484ada326894556ae499be4b38662227429687`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:f1c493023b4ed6d738f467fca7f0b2d92b95335adbda5b18bbe15b9af0ccb33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856c1affda75149a5241b1d28d1e6618599f3dbf59e5a63f7405a4307280290e`

```dockerfile
```

-	Layers:
	-	`sha256:e893b3d0edebe68f568f76cf8a8765526bd4f038336efa0e047540a58cc81ece`  
		Last Modified: Tue, 11 Nov 2025 06:07:35 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:0dea739e8da25364ad4b96de17ee4ca9ab3ee4b1853feaeb656908f9c2f15d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134122997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e965328256d5f24c1340bb8fe352992ce0115545213c85811d887055ce2b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:08:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:08:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:08:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:08:57 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231bfd4746adb8d80098ffe2b9e41c38b9b0f3b07364e636f24dfd181f529a3f`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 6.5 MB (6538231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430d5813d2cbd287f1f28c0b9beee442827ab11d4a8ebba2b422df8ab2fdfd5`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 86.4 KB (86387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790a160f5c3b286a104a10316a01fc4f087539c8ef1489b6fce21ad25dbda68c`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac758b28033ab99ed3d93e0a5d7e41217a07d02ff8c0d3a1c23956fdb0fa14`  
		Last Modified: Tue, 11 Nov 2025 02:09:28 GMT  
		Size: 58.1 MB (58057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9bc7f222c27d8695badee53831e2305c943e58fca76ed7ffee95a51ff4721`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998d611185d7cbaa4fe1b29c4c82e2f5c9b09c8070c2db204e04351d0c79981`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:3617129123778bb4c70edbed5f249717569f4ead11ad46b83e4885c3813775e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59faba2e7641334fc344c52dfee2abccbd797367db99d1ffb9e1dde06c5b5c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea82643619a2cc049ccf3cf5ecc7840bffdf522b8052b76245630ef2c73807a`  
		Last Modified: Tue, 11 Nov 2025 06:07:37 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:401d14a2f2adf4049a65a1e43a7015d6535f0a3d9fd3f4983eb2f7b8be34669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133608586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620363b32bc14b7498b2ea91462c609689f37821a91d113ea08c303a429d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:05658c0ee5399800317269e821d0af4f2bc594f25082f70dde54d05f1343ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c679cdfbd2c4de098f839b682a1d5ef1ec6a2dd2df6cf57164e9431bb6100a1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a07abadd15bdc841d4aca14903139ea1d3b06379b0c5b04895afc55c44d19c`  
		Last Modified: Tue, 11 Nov 2025 06:07:40 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:87858a6dd14149240f4a2c33e0ec0f32a5ac1bb2548c04f5a20694ea25cb6157
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
$ docker pull docker@sha256:85b69bff6696b21432c9a0c97d9ba577dcfa1abd09c2fe7064521f845db7ba10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74694027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b460f9e12dba9ee2f56aee0f01e5ec9fec819cd562fa6830d4cbe499cb90cfa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:edc7c416b5749e58ae06051f73f58941925ea0e92139cecb3942f82b66548726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ccd16ac07cf0e07f69b5389a4ddc6813b3cc6a9b6e36d4949cb95ac4501849`

```dockerfile
```

-	Layers:
	-	`sha256:a2cc848b3383a4812739dd031cc0bbeb7467ec96000656df5e9cde1d6d3f8633`  
		Last Modified: Tue, 11 Nov 2025 03:07:28 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:db6f1b09c83095931c62c38f3326c38fa50c08aaacfb883ef2690ba2732ba235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70439557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530b79b8ee9c418f2e9616e0ae46c306cbf27d8cef7cd84a6a9833cf7b003dfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8068d2a5a896fd79499397ab7f094ac12aa83ee4089f75aac6336e24e4691bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea34c81a23aa2af2ba356d98981809c05b67bff1ba3c9ea0d5172895744a0bbc`

```dockerfile
```

-	Layers:
	-	`sha256:e5d052648f543fb28f0fe4b56a4b0130450df95ad7ae79e57620bc144564b7f0`  
		Last Modified: Tue, 11 Nov 2025 03:07:31 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4ccec6e40933fa64d0334144f642a1e480f71a6780c4bc3eae361d3eb7cc39e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69434747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b0d5938bdacd4bb4fb88b45fca03668fa50596f84faaca883672554fca777f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:958bb6a5751db20fca83307e98779011066c11405ac2a69e134b82980c08d77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c097d20db918a54283a2ab06f3e60191ce4493c88229975725173c04bc393766`

```dockerfile
```

-	Layers:
	-	`sha256:f788d6efa84036126423fe4369987a8a51132192aed4ccb420682aa9c73fe7b9`  
		Last Modified: Tue, 11 Nov 2025 03:07:33 GMT  
		Size: 38.2 KB (38238 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fb78d3008a96342d542ed9cf971f8d4a833fd1efb7e514b580cb285fba8cf146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69865515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b61bf9d97253c23eb31dc71e0a54e61c41bf2e91d184b357502826e956d7d7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dfc45fa7a7ebd405ac76c818dd144712daa26778ce043a76705b59adadfbf594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89636110a73f7d0bb3efc7ccdf96f43e55da09947af75a3d39f5fc8e01817d7e`

```dockerfile
```

-	Layers:
	-	`sha256:67831bcf8526bf2bbe1929f191e97b780e4ffd6f8c224c78e07320a922349a82`  
		Last Modified: Tue, 11 Nov 2025 03:07:36 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:96789d56621ae702a2f8aa316c87a1a1875dd3f02bf67cdcb56a524a09fa3af9
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
$ docker pull docker@sha256:df7efe7183e533112a8236c5fddb1edf12c96fb2feba3b6b693a285bd7bb993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143957895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cdce60b4d9596765151d2508cad4e3441223cf71e32ba68015def44b654c2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bf82da9d97fb017eb52fe800bcb19e47f54474e8d981b8682beb615517afd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0164e514b2ea3e21ae8f8c5486cd2d19628d181877991e1232da20933c44b`

```dockerfile
```

-	Layers:
	-	`sha256:d474ac080071d8e06b197e991ae6cd69e0220b949c3e867e07644315c15c39d2`  
		Last Modified: Tue, 11 Nov 2025 06:07:32 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:801cd28b5bdd6f880f7551901af30f6f084bd70c09dffa4ca0d2cace1eba03af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135991944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c369e847de2b33daebebfd4b7581651530f43a5f1705341a2e0fd7e3f1090`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d9e03480f36684f99c499bcac854458fc59fbd5fa1590b2a75308769f18bf`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 7.2 MB (7230266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4413fdb49a4b4c681741a79c06d306c0adce974437e167ab302104c09817f74f`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 89.9 KB (89949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ef3e596708743d134b73dba182acb89d52baa28af431f822db748a0b6e68a7`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84002f98aaa912e73b1fefcb7d1eb964dde81fa74a2ecdb42592b3199151e4a`  
		Last Modified: Tue, 11 Nov 2025 02:10:03 GMT  
		Size: 58.2 MB (58226172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c833c392dc7ac6d8703b1d37c747c18bbb1a7b715d2310cb1714175f258eb28`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefbb114f52aff835ec78ec55484ada326894556ae499be4b38662227429687`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f1c493023b4ed6d738f467fca7f0b2d92b95335adbda5b18bbe15b9af0ccb33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856c1affda75149a5241b1d28d1e6618599f3dbf59e5a63f7405a4307280290e`

```dockerfile
```

-	Layers:
	-	`sha256:e893b3d0edebe68f568f76cf8a8765526bd4f038336efa0e047540a58cc81ece`  
		Last Modified: Tue, 11 Nov 2025 06:07:35 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0dea739e8da25364ad4b96de17ee4ca9ab3ee4b1853feaeb656908f9c2f15d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134122997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e965328256d5f24c1340bb8fe352992ce0115545213c85811d887055ce2b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:08:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:08:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:08:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:08:57 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231bfd4746adb8d80098ffe2b9e41c38b9b0f3b07364e636f24dfd181f529a3f`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 6.5 MB (6538231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430d5813d2cbd287f1f28c0b9beee442827ab11d4a8ebba2b422df8ab2fdfd5`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 86.4 KB (86387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790a160f5c3b286a104a10316a01fc4f087539c8ef1489b6fce21ad25dbda68c`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac758b28033ab99ed3d93e0a5d7e41217a07d02ff8c0d3a1c23956fdb0fa14`  
		Last Modified: Tue, 11 Nov 2025 02:09:28 GMT  
		Size: 58.1 MB (58057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9bc7f222c27d8695badee53831e2305c943e58fca76ed7ffee95a51ff4721`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998d611185d7cbaa4fe1b29c4c82e2f5c9b09c8070c2db204e04351d0c79981`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3617129123778bb4c70edbed5f249717569f4ead11ad46b83e4885c3813775e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59faba2e7641334fc344c52dfee2abccbd797367db99d1ffb9e1dde06c5b5c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea82643619a2cc049ccf3cf5ecc7840bffdf522b8052b76245630ef2c73807a`  
		Last Modified: Tue, 11 Nov 2025 06:07:37 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:401d14a2f2adf4049a65a1e43a7015d6535f0a3d9fd3f4983eb2f7b8be34669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133608586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620363b32bc14b7498b2ea91462c609689f37821a91d113ea08c303a429d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:05658c0ee5399800317269e821d0af4f2bc594f25082f70dde54d05f1343ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c679cdfbd2c4de098f839b682a1d5ef1ec6a2dd2df6cf57164e9431bb6100a1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a07abadd15bdc841d4aca14903139ea1d3b06379b0c5b04895afc55c44d19c`  
		Last Modified: Tue, 11 Nov 2025 06:07:40 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:655682420c390d78bdac672dc9d35667fa1e52a760680657f6d45589047602fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:42ff18328a31c104cd584f80bc4b226cc9758918dcc508665d6a1b95db855471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164727869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6546ea708bf60ea1e4ef3695c1216d35872e9d7c0b0e22ad42fe24c8875d78c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
# Tue, 11 Nov 2025 03:10:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 11 Nov 2025 03:10:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 11 Nov 2025 03:10:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 11 Nov 2025 03:10:11 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafcd68783d7705964732be0808bd0bb79510ff08a912dbafcc3fd7a22fb6cde`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 3.4 MB (3398393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877c138ce4f7a03c272f7263704eed9984e712511333124d8573865dcc29fc19`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f6919cf3ae19fe242e3ae3e2e69ba5fdad9b62ee1ba25e00d02f9ab008d2e8`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64635a629124d1d8a7e1ae88ae288f18e1979a129293587b291dffd3e2262bf0`  
		Last Modified: Tue, 11 Nov 2025 03:10:28 GMT  
		Size: 17.4 MB (17370240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ee1e48d6f34d4967b6e2533d92965d2ce3d9cb76988f11587335211d8dc6a4`  
		Last Modified: Tue, 11 Nov 2025 03:10:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ab78b124a9ff0ce7253385fe42b866700df87ec72d0c74762409d5a09fe1441d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3774ad7d79781a69ae44de5f03cba5564f606f9c9cbfe569307486299cd910`

```dockerfile
```

-	Layers:
	-	`sha256:0067f650317a33b012070bdb14ddb432839900e99f3ed8642730f12baf986d52`  
		Last Modified: Tue, 11 Nov 2025 06:07:46 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ea7d11c209f5f9c6c6b0299573681a3ad6032cbcbf24d22fbf8bf913961591db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154706892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb198c77d75eea1b7edffcac43925972fa2a02d4280a799c54cb052f39ed2229`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
# Tue, 11 Nov 2025 03:09:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 11 Nov 2025 03:09:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 11 Nov 2025 03:09:52 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 11 Nov 2025 03:09:53 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcb06fab37a52d9a24735f766783d73c09eb40a62c6b55aad8e566ab5cc722c`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 3.4 MB (3389934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264ee650ea75362a13bdaaf8fde957d1a108659352e29da95c8e5b9068bbee38`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca921cac3d58424a9d678c45dc156d4979e295b0b8bcc70b563adaf098d26484`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3eeaf9a370146e91d691c000c720b150c79437f704b1f1a2ad15fb331dff742`  
		Last Modified: Tue, 11 Nov 2025 03:10:12 GMT  
		Size: 17.7 MB (17707031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e43df59a31a48918f41ad14da8cca78b0b51f4d960b632a4e97f489ba38a45`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c09f760ea44c49943c419da5b2673f21ffbb51a0aff0fdd1e846779a8799a600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e8551cb7c3cdaf5e80a2b47160a8c65c3d4ed6d7db3b6e82aebd9e41281bf1`

```dockerfile
```

-	Layers:
	-	`sha256:3033c8a433fb48e4ad4962e0385738ce667cdb9d654449c9c648c59dd437e1d5`  
		Last Modified: Tue, 11 Nov 2025 06:07:49 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:72d299112395e5cec5a7ae09c7e757b1c70362702ec37656206b365f8e81580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:d3430dae25034c55c56dd585271ca3ff7633e012a1ba11f1498b04f25693ef2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3286034630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d734e887c89ba0c951f704dfa1208365d6a2457d51ed341c05d8223c37bd652a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Tue, 11 Nov 2025 01:09:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:09:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:09:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:09:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:09:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:09:59 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:10:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:10:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:10:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cbb13e31831b4a401483474d0b3761d526123e4940ffefb9e59ca0b95bd928`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11778e4fa17626dc91d9d9cb467403166f0cc6134bcadc2c6c394c23f4f77350`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 385.3 KB (385346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea88d46cd119b0ed069843b33c117aa143e9f6c36695cf17ee648d8dcf3655b`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa5fa37b5931fe92505e086ba67d6dfb0da4ae0172b58b04d5bb013277f60b9`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ada5899e6769690fd204f9f137706c9612fa97a65835249036bb92593e5eb`  
		Last Modified: Tue, 11 Nov 2025 01:19:20 GMT  
		Size: 19.4 MB (19430246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0272441663d6fec957c0b4d34b58b8a19b8808f1771c45d4c591dff46cb951`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918e1ab8b826581917ab7b2d53b2c6a5f2b06ce5c03f208c14dea008b3cfe60`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce36d1376a231ae8f91e59637fe876b6fa19bccb1bfd0a4e96c4d2b5d24a5ae5`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f749f808cf8c30f6a915e56d9393b185ef4a06c9ab0ce38fab25952828f43c6d`  
		Last Modified: Tue, 11 Nov 2025 01:19:18 GMT  
		Size: 23.2 MB (23173614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4c6efb8d391dc41567c8e29c5f2c1aaa0d6372c5dab092454b25133fbaf22`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f789efcc4cd75dab1e0486cceffa4fbb47564e174bfb011d328003e81c690ad`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73f4b7bd98ba3e36992613125ce4ea0186486089e65bd5b3be8e14604b916f0`  
		Last Modified: Tue, 11 Nov 2025 01:19:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ae4ce13bc5f392ee40f76f48ccf05ef5a576bd04b4b7affecfadde7443a36`  
		Last Modified: Tue, 11 Nov 2025 01:19:22 GMT  
		Size: 22.7 MB (22686606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:4da74ebb24ba1ed05d837769e2868b3fced76e9d625b5033e5c6bd554dba5b1c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1642975859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b248f8970d471ca71d2fe5d8cf5a618741a9ae195807e67894fa707304be22f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Tue, 11 Nov 2025 01:31:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:32:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:32:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:32:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:33:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:08 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:33:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:33:10 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:33:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:33:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607358d94499b322187d8294abffa374df336a542ba3a7746e54550a559a84e3`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff233fc8be81f08e0fd27b16161e9cb9e883edbeeb55293e4f90cf045577ee6b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 510.8 KB (510798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5647cb091467ce953f8492c583014320a568592f5d1f5685de40d7c64f5e5fe8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45373dae92aa5007d34f749e78b0e5899e1a7c3c1ce4329315c3a5d7969c469b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cffa7afe37dfd330f9aa05e82a6f05a309d0d2079e615fcab933f7b9ead0d7`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 19.4 MB (19419747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f4ab1b20e761366e4592a4a695a67d6fb6ad55c780094fad9976df3ebeb21`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477c725c69905fa95c18552eb154560a212870c86cb468c7570ef9beea16e8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade21b9c6cec037cb7d2f205612a41a75789f0857a3304753e001984561e9983`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7311ebb09d47c704ac9a5d171113840b634120dc0c680eb276a91ddee2efd`  
		Last Modified: Tue, 11 Nov 2025 01:44:35 GMT  
		Size: 23.2 MB (23163257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28603a23c96e1bd9ba9ee0b8e4c446e6e01e8f268c3b8a292c4b7749184649d5`  
		Last Modified: Tue, 11 Nov 2025 01:44:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e94373564db23e5d8ea9cc012d861df363325d542c9908aee4273fe0a84566`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c07acbdd0f1cc9183784756376bc05490f3e9257490fc0a387eceb8ff38c645`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be490461e18aba4834222d552c012a6093108c1e590650b34829a457e978bc8c`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 22.7 MB (22677281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9c96d3736d1657483916877049c0ccbdb057a8df315fcb3e663048acfbd132d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:4da74ebb24ba1ed05d837769e2868b3fced76e9d625b5033e5c6bd554dba5b1c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1642975859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b248f8970d471ca71d2fe5d8cf5a618741a9ae195807e67894fa707304be22f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Tue, 11 Nov 2025 01:31:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:32:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:32:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:32:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:33:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:08 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:33:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:33:10 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:33:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:33:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607358d94499b322187d8294abffa374df336a542ba3a7746e54550a559a84e3`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff233fc8be81f08e0fd27b16161e9cb9e883edbeeb55293e4f90cf045577ee6b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 510.8 KB (510798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5647cb091467ce953f8492c583014320a568592f5d1f5685de40d7c64f5e5fe8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45373dae92aa5007d34f749e78b0e5899e1a7c3c1ce4329315c3a5d7969c469b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cffa7afe37dfd330f9aa05e82a6f05a309d0d2079e615fcab933f7b9ead0d7`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 19.4 MB (19419747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f4ab1b20e761366e4592a4a695a67d6fb6ad55c780094fad9976df3ebeb21`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477c725c69905fa95c18552eb154560a212870c86cb468c7570ef9beea16e8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade21b9c6cec037cb7d2f205612a41a75789f0857a3304753e001984561e9983`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7311ebb09d47c704ac9a5d171113840b634120dc0c680eb276a91ddee2efd`  
		Last Modified: Tue, 11 Nov 2025 01:44:35 GMT  
		Size: 23.2 MB (23163257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28603a23c96e1bd9ba9ee0b8e4c446e6e01e8f268c3b8a292c4b7749184649d5`  
		Last Modified: Tue, 11 Nov 2025 01:44:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e94373564db23e5d8ea9cc012d861df363325d542c9908aee4273fe0a84566`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c07acbdd0f1cc9183784756376bc05490f3e9257490fc0a387eceb8ff38c645`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be490461e18aba4834222d552c012a6093108c1e590650b34829a457e978bc8c`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 22.7 MB (22677281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:cf52fc75c50a0b3ee0fd34f484cb9e7aa12c6b6f6187e520f1fc9cb2a96807fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:d3430dae25034c55c56dd585271ca3ff7633e012a1ba11f1498b04f25693ef2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3286034630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d734e887c89ba0c951f704dfa1208365d6a2457d51ed341c05d8223c37bd652a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Tue, 11 Nov 2025 01:09:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:09:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:09:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:09:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:09:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:09:59 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:10:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:10:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:10:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cbb13e31831b4a401483474d0b3761d526123e4940ffefb9e59ca0b95bd928`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11778e4fa17626dc91d9d9cb467403166f0cc6134bcadc2c6c394c23f4f77350`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 385.3 KB (385346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea88d46cd119b0ed069843b33c117aa143e9f6c36695cf17ee648d8dcf3655b`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa5fa37b5931fe92505e086ba67d6dfb0da4ae0172b58b04d5bb013277f60b9`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ada5899e6769690fd204f9f137706c9612fa97a65835249036bb92593e5eb`  
		Last Modified: Tue, 11 Nov 2025 01:19:20 GMT  
		Size: 19.4 MB (19430246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0272441663d6fec957c0b4d34b58b8a19b8808f1771c45d4c591dff46cb951`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918e1ab8b826581917ab7b2d53b2c6a5f2b06ce5c03f208c14dea008b3cfe60`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce36d1376a231ae8f91e59637fe876b6fa19bccb1bfd0a4e96c4d2b5d24a5ae5`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f749f808cf8c30f6a915e56d9393b185ef4a06c9ab0ce38fab25952828f43c6d`  
		Last Modified: Tue, 11 Nov 2025 01:19:18 GMT  
		Size: 23.2 MB (23173614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4c6efb8d391dc41567c8e29c5f2c1aaa0d6372c5dab092454b25133fbaf22`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f789efcc4cd75dab1e0486cceffa4fbb47564e174bfb011d328003e81c690ad`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73f4b7bd98ba3e36992613125ce4ea0186486089e65bd5b3be8e14604b916f0`  
		Last Modified: Tue, 11 Nov 2025 01:19:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ae4ce13bc5f392ee40f76f48ccf05ef5a576bd04b4b7affecfadde7443a36`  
		Last Modified: Tue, 11 Nov 2025 01:19:22 GMT  
		Size: 22.7 MB (22686606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0`

```console
$ docker pull docker@sha256:96789d56621ae702a2f8aa316c87a1a1875dd3f02bf67cdcb56a524a09fa3af9
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

### `docker:29.0` - linux; amd64

```console
$ docker pull docker@sha256:df7efe7183e533112a8236c5fddb1edf12c96fb2feba3b6b693a285bd7bb993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143957895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cdce60b4d9596765151d2508cad4e3441223cf71e32ba68015def44b654c2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0` - unknown; unknown

```console
$ docker pull docker@sha256:bf82da9d97fb017eb52fe800bcb19e47f54474e8d981b8682beb615517afd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0164e514b2ea3e21ae8f8c5486cd2d19628d181877991e1232da20933c44b`

```dockerfile
```

-	Layers:
	-	`sha256:d474ac080071d8e06b197e991ae6cd69e0220b949c3e867e07644315c15c39d2`  
		Last Modified: Tue, 11 Nov 2025 06:07:32 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:801cd28b5bdd6f880f7551901af30f6f084bd70c09dffa4ca0d2cace1eba03af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135991944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c369e847de2b33daebebfd4b7581651530f43a5f1705341a2e0fd7e3f1090`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d9e03480f36684f99c499bcac854458fc59fbd5fa1590b2a75308769f18bf`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 7.2 MB (7230266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4413fdb49a4b4c681741a79c06d306c0adce974437e167ab302104c09817f74f`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 89.9 KB (89949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ef3e596708743d134b73dba182acb89d52baa28af431f822db748a0b6e68a7`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84002f98aaa912e73b1fefcb7d1eb964dde81fa74a2ecdb42592b3199151e4a`  
		Last Modified: Tue, 11 Nov 2025 02:10:03 GMT  
		Size: 58.2 MB (58226172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c833c392dc7ac6d8703b1d37c747c18bbb1a7b715d2310cb1714175f258eb28`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefbb114f52aff835ec78ec55484ada326894556ae499be4b38662227429687`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0` - unknown; unknown

```console
$ docker pull docker@sha256:f1c493023b4ed6d738f467fca7f0b2d92b95335adbda5b18bbe15b9af0ccb33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856c1affda75149a5241b1d28d1e6618599f3dbf59e5a63f7405a4307280290e`

```dockerfile
```

-	Layers:
	-	`sha256:e893b3d0edebe68f568f76cf8a8765526bd4f038336efa0e047540a58cc81ece`  
		Last Modified: Tue, 11 Nov 2025 06:07:35 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:0dea739e8da25364ad4b96de17ee4ca9ab3ee4b1853feaeb656908f9c2f15d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134122997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e965328256d5f24c1340bb8fe352992ce0115545213c85811d887055ce2b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:08:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:08:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:08:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:08:57 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231bfd4746adb8d80098ffe2b9e41c38b9b0f3b07364e636f24dfd181f529a3f`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 6.5 MB (6538231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430d5813d2cbd287f1f28c0b9beee442827ab11d4a8ebba2b422df8ab2fdfd5`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 86.4 KB (86387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790a160f5c3b286a104a10316a01fc4f087539c8ef1489b6fce21ad25dbda68c`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac758b28033ab99ed3d93e0a5d7e41217a07d02ff8c0d3a1c23956fdb0fa14`  
		Last Modified: Tue, 11 Nov 2025 02:09:28 GMT  
		Size: 58.1 MB (58057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9bc7f222c27d8695badee53831e2305c943e58fca76ed7ffee95a51ff4721`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998d611185d7cbaa4fe1b29c4c82e2f5c9b09c8070c2db204e04351d0c79981`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0` - unknown; unknown

```console
$ docker pull docker@sha256:3617129123778bb4c70edbed5f249717569f4ead11ad46b83e4885c3813775e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59faba2e7641334fc344c52dfee2abccbd797367db99d1ffb9e1dde06c5b5c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea82643619a2cc049ccf3cf5ecc7840bffdf522b8052b76245630ef2c73807a`  
		Last Modified: Tue, 11 Nov 2025 06:07:37 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:401d14a2f2adf4049a65a1e43a7015d6535f0a3d9fd3f4983eb2f7b8be34669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133608586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620363b32bc14b7498b2ea91462c609689f37821a91d113ea08c303a429d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0` - unknown; unknown

```console
$ docker pull docker@sha256:05658c0ee5399800317269e821d0af4f2bc594f25082f70dde54d05f1343ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c679cdfbd2c4de098f839b682a1d5ef1ec6a2dd2df6cf57164e9431bb6100a1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a07abadd15bdc841d4aca14903139ea1d3b06379b0c5b04895afc55c44d19c`  
		Last Modified: Tue, 11 Nov 2025 06:07:40 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0-cli`

```console
$ docker pull docker@sha256:87858a6dd14149240f4a2c33e0ec0f32a5ac1bb2548c04f5a20694ea25cb6157
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

### `docker:29.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:85b69bff6696b21432c9a0c97d9ba577dcfa1abd09c2fe7064521f845db7ba10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74694027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b460f9e12dba9ee2f56aee0f01e5ec9fec819cd562fa6830d4cbe499cb90cfa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:edc7c416b5749e58ae06051f73f58941925ea0e92139cecb3942f82b66548726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ccd16ac07cf0e07f69b5389a4ddc6813b3cc6a9b6e36d4949cb95ac4501849`

```dockerfile
```

-	Layers:
	-	`sha256:a2cc848b3383a4812739dd031cc0bbeb7467ec96000656df5e9cde1d6d3f8633`  
		Last Modified: Tue, 11 Nov 2025 03:07:28 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:db6f1b09c83095931c62c38f3326c38fa50c08aaacfb883ef2690ba2732ba235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70439557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530b79b8ee9c418f2e9616e0ae46c306cbf27d8cef7cd84a6a9833cf7b003dfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8068d2a5a896fd79499397ab7f094ac12aa83ee4089f75aac6336e24e4691bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea34c81a23aa2af2ba356d98981809c05b67bff1ba3c9ea0d5172895744a0bbc`

```dockerfile
```

-	Layers:
	-	`sha256:e5d052648f543fb28f0fe4b56a4b0130450df95ad7ae79e57620bc144564b7f0`  
		Last Modified: Tue, 11 Nov 2025 03:07:31 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4ccec6e40933fa64d0334144f642a1e480f71a6780c4bc3eae361d3eb7cc39e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69434747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b0d5938bdacd4bb4fb88b45fca03668fa50596f84faaca883672554fca777f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:958bb6a5751db20fca83307e98779011066c11405ac2a69e134b82980c08d77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c097d20db918a54283a2ab06f3e60191ce4493c88229975725173c04bc393766`

```dockerfile
```

-	Layers:
	-	`sha256:f788d6efa84036126423fe4369987a8a51132192aed4ccb420682aa9c73fe7b9`  
		Last Modified: Tue, 11 Nov 2025 03:07:33 GMT  
		Size: 38.2 KB (38238 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fb78d3008a96342d542ed9cf971f8d4a833fd1efb7e514b580cb285fba8cf146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69865515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b61bf9d97253c23eb31dc71e0a54e61c41bf2e91d184b357502826e956d7d7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dfc45fa7a7ebd405ac76c818dd144712daa26778ce043a76705b59adadfbf594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89636110a73f7d0bb3efc7ccdf96f43e55da09947af75a3d39f5fc8e01817d7e`

```dockerfile
```

-	Layers:
	-	`sha256:67831bcf8526bf2bbe1929f191e97b780e4ffd6f8c224c78e07320a922349a82`  
		Last Modified: Tue, 11 Nov 2025 03:07:36 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0-dind`

```console
$ docker pull docker@sha256:96789d56621ae702a2f8aa316c87a1a1875dd3f02bf67cdcb56a524a09fa3af9
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

### `docker:29.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:df7efe7183e533112a8236c5fddb1edf12c96fb2feba3b6b693a285bd7bb993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143957895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cdce60b4d9596765151d2508cad4e3441223cf71e32ba68015def44b654c2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bf82da9d97fb017eb52fe800bcb19e47f54474e8d981b8682beb615517afd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0164e514b2ea3e21ae8f8c5486cd2d19628d181877991e1232da20933c44b`

```dockerfile
```

-	Layers:
	-	`sha256:d474ac080071d8e06b197e991ae6cd69e0220b949c3e867e07644315c15c39d2`  
		Last Modified: Tue, 11 Nov 2025 06:07:32 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:801cd28b5bdd6f880f7551901af30f6f084bd70c09dffa4ca0d2cace1eba03af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135991944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c369e847de2b33daebebfd4b7581651530f43a5f1705341a2e0fd7e3f1090`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d9e03480f36684f99c499bcac854458fc59fbd5fa1590b2a75308769f18bf`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 7.2 MB (7230266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4413fdb49a4b4c681741a79c06d306c0adce974437e167ab302104c09817f74f`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 89.9 KB (89949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ef3e596708743d134b73dba182acb89d52baa28af431f822db748a0b6e68a7`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84002f98aaa912e73b1fefcb7d1eb964dde81fa74a2ecdb42592b3199151e4a`  
		Last Modified: Tue, 11 Nov 2025 02:10:03 GMT  
		Size: 58.2 MB (58226172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c833c392dc7ac6d8703b1d37c747c18bbb1a7b715d2310cb1714175f258eb28`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefbb114f52aff835ec78ec55484ada326894556ae499be4b38662227429687`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f1c493023b4ed6d738f467fca7f0b2d92b95335adbda5b18bbe15b9af0ccb33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856c1affda75149a5241b1d28d1e6618599f3dbf59e5a63f7405a4307280290e`

```dockerfile
```

-	Layers:
	-	`sha256:e893b3d0edebe68f568f76cf8a8765526bd4f038336efa0e047540a58cc81ece`  
		Last Modified: Tue, 11 Nov 2025 06:07:35 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0dea739e8da25364ad4b96de17ee4ca9ab3ee4b1853feaeb656908f9c2f15d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134122997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e965328256d5f24c1340bb8fe352992ce0115545213c85811d887055ce2b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:08:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:08:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:08:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:08:57 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231bfd4746adb8d80098ffe2b9e41c38b9b0f3b07364e636f24dfd181f529a3f`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 6.5 MB (6538231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430d5813d2cbd287f1f28c0b9beee442827ab11d4a8ebba2b422df8ab2fdfd5`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 86.4 KB (86387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790a160f5c3b286a104a10316a01fc4f087539c8ef1489b6fce21ad25dbda68c`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac758b28033ab99ed3d93e0a5d7e41217a07d02ff8c0d3a1c23956fdb0fa14`  
		Last Modified: Tue, 11 Nov 2025 02:09:28 GMT  
		Size: 58.1 MB (58057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9bc7f222c27d8695badee53831e2305c943e58fca76ed7ffee95a51ff4721`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998d611185d7cbaa4fe1b29c4c82e2f5c9b09c8070c2db204e04351d0c79981`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3617129123778bb4c70edbed5f249717569f4ead11ad46b83e4885c3813775e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59faba2e7641334fc344c52dfee2abccbd797367db99d1ffb9e1dde06c5b5c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea82643619a2cc049ccf3cf5ecc7840bffdf522b8052b76245630ef2c73807a`  
		Last Modified: Tue, 11 Nov 2025 06:07:37 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:401d14a2f2adf4049a65a1e43a7015d6535f0a3d9fd3f4983eb2f7b8be34669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133608586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620363b32bc14b7498b2ea91462c609689f37821a91d113ea08c303a429d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:05658c0ee5399800317269e821d0af4f2bc594f25082f70dde54d05f1343ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c679cdfbd2c4de098f839b682a1d5ef1ec6a2dd2df6cf57164e9431bb6100a1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a07abadd15bdc841d4aca14903139ea1d3b06379b0c5b04895afc55c44d19c`  
		Last Modified: Tue, 11 Nov 2025 06:07:40 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0-dind-rootless`

```console
$ docker pull docker@sha256:655682420c390d78bdac672dc9d35667fa1e52a760680657f6d45589047602fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:42ff18328a31c104cd584f80bc4b226cc9758918dcc508665d6a1b95db855471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164727869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6546ea708bf60ea1e4ef3695c1216d35872e9d7c0b0e22ad42fe24c8875d78c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
# Tue, 11 Nov 2025 03:10:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 11 Nov 2025 03:10:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 11 Nov 2025 03:10:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 11 Nov 2025 03:10:11 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafcd68783d7705964732be0808bd0bb79510ff08a912dbafcc3fd7a22fb6cde`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 3.4 MB (3398393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877c138ce4f7a03c272f7263704eed9984e712511333124d8573865dcc29fc19`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f6919cf3ae19fe242e3ae3e2e69ba5fdad9b62ee1ba25e00d02f9ab008d2e8`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64635a629124d1d8a7e1ae88ae288f18e1979a129293587b291dffd3e2262bf0`  
		Last Modified: Tue, 11 Nov 2025 03:10:28 GMT  
		Size: 17.4 MB (17370240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ee1e48d6f34d4967b6e2533d92965d2ce3d9cb76988f11587335211d8dc6a4`  
		Last Modified: Tue, 11 Nov 2025 03:10:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ab78b124a9ff0ce7253385fe42b866700df87ec72d0c74762409d5a09fe1441d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3774ad7d79781a69ae44de5f03cba5564f606f9c9cbfe569307486299cd910`

```dockerfile
```

-	Layers:
	-	`sha256:0067f650317a33b012070bdb14ddb432839900e99f3ed8642730f12baf986d52`  
		Last Modified: Tue, 11 Nov 2025 06:07:46 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ea7d11c209f5f9c6c6b0299573681a3ad6032cbcbf24d22fbf8bf913961591db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154706892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb198c77d75eea1b7edffcac43925972fa2a02d4280a799c54cb052f39ed2229`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
# Tue, 11 Nov 2025 03:09:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 11 Nov 2025 03:09:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 11 Nov 2025 03:09:52 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 11 Nov 2025 03:09:53 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcb06fab37a52d9a24735f766783d73c09eb40a62c6b55aad8e566ab5cc722c`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 3.4 MB (3389934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264ee650ea75362a13bdaaf8fde957d1a108659352e29da95c8e5b9068bbee38`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca921cac3d58424a9d678c45dc156d4979e295b0b8bcc70b563adaf098d26484`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3eeaf9a370146e91d691c000c720b150c79437f704b1f1a2ad15fb331dff742`  
		Last Modified: Tue, 11 Nov 2025 03:10:12 GMT  
		Size: 17.7 MB (17707031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e43df59a31a48918f41ad14da8cca78b0b51f4d960b632a4e97f489ba38a45`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c09f760ea44c49943c419da5b2673f21ffbb51a0aff0fdd1e846779a8799a600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e8551cb7c3cdaf5e80a2b47160a8c65c3d4ed6d7db3b6e82aebd9e41281bf1`

```dockerfile
```

-	Layers:
	-	`sha256:3033c8a433fb48e4ad4962e0385738ce667cdb9d654449c9c648c59dd437e1d5`  
		Last Modified: Tue, 11 Nov 2025 06:07:49 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0-windowsservercore`

```console
$ docker pull docker@sha256:72d299112395e5cec5a7ae09c7e757b1c70362702ec37656206b365f8e81580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `docker:29.0-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:d3430dae25034c55c56dd585271ca3ff7633e012a1ba11f1498b04f25693ef2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3286034630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d734e887c89ba0c951f704dfa1208365d6a2457d51ed341c05d8223c37bd652a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Tue, 11 Nov 2025 01:09:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:09:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:09:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:09:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:09:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:09:59 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:10:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:10:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:10:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cbb13e31831b4a401483474d0b3761d526123e4940ffefb9e59ca0b95bd928`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11778e4fa17626dc91d9d9cb467403166f0cc6134bcadc2c6c394c23f4f77350`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 385.3 KB (385346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea88d46cd119b0ed069843b33c117aa143e9f6c36695cf17ee648d8dcf3655b`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa5fa37b5931fe92505e086ba67d6dfb0da4ae0172b58b04d5bb013277f60b9`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ada5899e6769690fd204f9f137706c9612fa97a65835249036bb92593e5eb`  
		Last Modified: Tue, 11 Nov 2025 01:19:20 GMT  
		Size: 19.4 MB (19430246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0272441663d6fec957c0b4d34b58b8a19b8808f1771c45d4c591dff46cb951`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918e1ab8b826581917ab7b2d53b2c6a5f2b06ce5c03f208c14dea008b3cfe60`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce36d1376a231ae8f91e59637fe876b6fa19bccb1bfd0a4e96c4d2b5d24a5ae5`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f749f808cf8c30f6a915e56d9393b185ef4a06c9ab0ce38fab25952828f43c6d`  
		Last Modified: Tue, 11 Nov 2025 01:19:18 GMT  
		Size: 23.2 MB (23173614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4c6efb8d391dc41567c8e29c5f2c1aaa0d6372c5dab092454b25133fbaf22`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f789efcc4cd75dab1e0486cceffa4fbb47564e174bfb011d328003e81c690ad`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73f4b7bd98ba3e36992613125ce4ea0186486089e65bd5b3be8e14604b916f0`  
		Last Modified: Tue, 11 Nov 2025 01:19:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ae4ce13bc5f392ee40f76f48ccf05ef5a576bd04b4b7affecfadde7443a36`  
		Last Modified: Tue, 11 Nov 2025 01:19:22 GMT  
		Size: 22.7 MB (22686606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.0-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:4da74ebb24ba1ed05d837769e2868b3fced76e9d625b5033e5c6bd554dba5b1c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1642975859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b248f8970d471ca71d2fe5d8cf5a618741a9ae195807e67894fa707304be22f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Tue, 11 Nov 2025 01:31:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:32:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:32:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:32:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:33:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:08 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:33:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:33:10 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:33:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:33:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607358d94499b322187d8294abffa374df336a542ba3a7746e54550a559a84e3`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff233fc8be81f08e0fd27b16161e9cb9e883edbeeb55293e4f90cf045577ee6b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 510.8 KB (510798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5647cb091467ce953f8492c583014320a568592f5d1f5685de40d7c64f5e5fe8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45373dae92aa5007d34f749e78b0e5899e1a7c3c1ce4329315c3a5d7969c469b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cffa7afe37dfd330f9aa05e82a6f05a309d0d2079e615fcab933f7b9ead0d7`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 19.4 MB (19419747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f4ab1b20e761366e4592a4a695a67d6fb6ad55c780094fad9976df3ebeb21`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477c725c69905fa95c18552eb154560a212870c86cb468c7570ef9beea16e8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade21b9c6cec037cb7d2f205612a41a75789f0857a3304753e001984561e9983`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7311ebb09d47c704ac9a5d171113840b634120dc0c680eb276a91ddee2efd`  
		Last Modified: Tue, 11 Nov 2025 01:44:35 GMT  
		Size: 23.2 MB (23163257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28603a23c96e1bd9ba9ee0b8e4c446e6e01e8f268c3b8a292c4b7749184649d5`  
		Last Modified: Tue, 11 Nov 2025 01:44:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e94373564db23e5d8ea9cc012d861df363325d542c9908aee4273fe0a84566`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c07acbdd0f1cc9183784756376bc05490f3e9257490fc0a387eceb8ff38c645`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be490461e18aba4834222d552c012a6093108c1e590650b34829a457e978bc8c`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 22.7 MB (22677281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9c96d3736d1657483916877049c0ccbdb057a8df315fcb3e663048acfbd132d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `docker:29.0-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:4da74ebb24ba1ed05d837769e2868b3fced76e9d625b5033e5c6bd554dba5b1c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1642975859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b248f8970d471ca71d2fe5d8cf5a618741a9ae195807e67894fa707304be22f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Tue, 11 Nov 2025 01:31:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:32:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:32:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:32:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:33:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:08 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:33:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:33:10 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:33:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:33:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607358d94499b322187d8294abffa374df336a542ba3a7746e54550a559a84e3`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff233fc8be81f08e0fd27b16161e9cb9e883edbeeb55293e4f90cf045577ee6b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 510.8 KB (510798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5647cb091467ce953f8492c583014320a568592f5d1f5685de40d7c64f5e5fe8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45373dae92aa5007d34f749e78b0e5899e1a7c3c1ce4329315c3a5d7969c469b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cffa7afe37dfd330f9aa05e82a6f05a309d0d2079e615fcab933f7b9ead0d7`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 19.4 MB (19419747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f4ab1b20e761366e4592a4a695a67d6fb6ad55c780094fad9976df3ebeb21`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477c725c69905fa95c18552eb154560a212870c86cb468c7570ef9beea16e8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade21b9c6cec037cb7d2f205612a41a75789f0857a3304753e001984561e9983`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7311ebb09d47c704ac9a5d171113840b634120dc0c680eb276a91ddee2efd`  
		Last Modified: Tue, 11 Nov 2025 01:44:35 GMT  
		Size: 23.2 MB (23163257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28603a23c96e1bd9ba9ee0b8e4c446e6e01e8f268c3b8a292c4b7749184649d5`  
		Last Modified: Tue, 11 Nov 2025 01:44:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e94373564db23e5d8ea9cc012d861df363325d542c9908aee4273fe0a84566`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c07acbdd0f1cc9183784756376bc05490f3e9257490fc0a387eceb8ff38c645`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be490461e18aba4834222d552c012a6093108c1e590650b34829a457e978bc8c`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 22.7 MB (22677281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:cf52fc75c50a0b3ee0fd34f484cb9e7aa12c6b6f6187e520f1fc9cb2a96807fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `docker:29.0-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:d3430dae25034c55c56dd585271ca3ff7633e012a1ba11f1498b04f25693ef2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3286034630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d734e887c89ba0c951f704dfa1208365d6a2457d51ed341c05d8223c37bd652a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Tue, 11 Nov 2025 01:09:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:09:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:09:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:09:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:09:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:09:59 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:10:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:10:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:10:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cbb13e31831b4a401483474d0b3761d526123e4940ffefb9e59ca0b95bd928`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11778e4fa17626dc91d9d9cb467403166f0cc6134bcadc2c6c394c23f4f77350`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 385.3 KB (385346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea88d46cd119b0ed069843b33c117aa143e9f6c36695cf17ee648d8dcf3655b`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa5fa37b5931fe92505e086ba67d6dfb0da4ae0172b58b04d5bb013277f60b9`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ada5899e6769690fd204f9f137706c9612fa97a65835249036bb92593e5eb`  
		Last Modified: Tue, 11 Nov 2025 01:19:20 GMT  
		Size: 19.4 MB (19430246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0272441663d6fec957c0b4d34b58b8a19b8808f1771c45d4c591dff46cb951`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918e1ab8b826581917ab7b2d53b2c6a5f2b06ce5c03f208c14dea008b3cfe60`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce36d1376a231ae8f91e59637fe876b6fa19bccb1bfd0a4e96c4d2b5d24a5ae5`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f749f808cf8c30f6a915e56d9393b185ef4a06c9ab0ce38fab25952828f43c6d`  
		Last Modified: Tue, 11 Nov 2025 01:19:18 GMT  
		Size: 23.2 MB (23173614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4c6efb8d391dc41567c8e29c5f2c1aaa0d6372c5dab092454b25133fbaf22`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f789efcc4cd75dab1e0486cceffa4fbb47564e174bfb011d328003e81c690ad`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73f4b7bd98ba3e36992613125ce4ea0186486089e65bd5b3be8e14604b916f0`  
		Last Modified: Tue, 11 Nov 2025 01:19:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ae4ce13bc5f392ee40f76f48ccf05ef5a576bd04b4b7affecfadde7443a36`  
		Last Modified: Tue, 11 Nov 2025 01:19:22 GMT  
		Size: 22.7 MB (22686606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0.0`

```console
$ docker pull docker@sha256:96789d56621ae702a2f8aa316c87a1a1875dd3f02bf67cdcb56a524a09fa3af9
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

### `docker:29.0.0` - linux; amd64

```console
$ docker pull docker@sha256:df7efe7183e533112a8236c5fddb1edf12c96fb2feba3b6b693a285bd7bb993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143957895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cdce60b4d9596765151d2508cad4e3441223cf71e32ba68015def44b654c2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0` - unknown; unknown

```console
$ docker pull docker@sha256:bf82da9d97fb017eb52fe800bcb19e47f54474e8d981b8682beb615517afd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0164e514b2ea3e21ae8f8c5486cd2d19628d181877991e1232da20933c44b`

```dockerfile
```

-	Layers:
	-	`sha256:d474ac080071d8e06b197e991ae6cd69e0220b949c3e867e07644315c15c39d2`  
		Last Modified: Tue, 11 Nov 2025 06:07:32 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:801cd28b5bdd6f880f7551901af30f6f084bd70c09dffa4ca0d2cace1eba03af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135991944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c369e847de2b33daebebfd4b7581651530f43a5f1705341a2e0fd7e3f1090`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d9e03480f36684f99c499bcac854458fc59fbd5fa1590b2a75308769f18bf`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 7.2 MB (7230266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4413fdb49a4b4c681741a79c06d306c0adce974437e167ab302104c09817f74f`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 89.9 KB (89949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ef3e596708743d134b73dba182acb89d52baa28af431f822db748a0b6e68a7`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84002f98aaa912e73b1fefcb7d1eb964dde81fa74a2ecdb42592b3199151e4a`  
		Last Modified: Tue, 11 Nov 2025 02:10:03 GMT  
		Size: 58.2 MB (58226172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c833c392dc7ac6d8703b1d37c747c18bbb1a7b715d2310cb1714175f258eb28`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefbb114f52aff835ec78ec55484ada326894556ae499be4b38662227429687`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0` - unknown; unknown

```console
$ docker pull docker@sha256:f1c493023b4ed6d738f467fca7f0b2d92b95335adbda5b18bbe15b9af0ccb33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856c1affda75149a5241b1d28d1e6618599f3dbf59e5a63f7405a4307280290e`

```dockerfile
```

-	Layers:
	-	`sha256:e893b3d0edebe68f568f76cf8a8765526bd4f038336efa0e047540a58cc81ece`  
		Last Modified: Tue, 11 Nov 2025 06:07:35 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:0dea739e8da25364ad4b96de17ee4ca9ab3ee4b1853feaeb656908f9c2f15d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134122997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e965328256d5f24c1340bb8fe352992ce0115545213c85811d887055ce2b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:08:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:08:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:08:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:08:57 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231bfd4746adb8d80098ffe2b9e41c38b9b0f3b07364e636f24dfd181f529a3f`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 6.5 MB (6538231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430d5813d2cbd287f1f28c0b9beee442827ab11d4a8ebba2b422df8ab2fdfd5`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 86.4 KB (86387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790a160f5c3b286a104a10316a01fc4f087539c8ef1489b6fce21ad25dbda68c`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac758b28033ab99ed3d93e0a5d7e41217a07d02ff8c0d3a1c23956fdb0fa14`  
		Last Modified: Tue, 11 Nov 2025 02:09:28 GMT  
		Size: 58.1 MB (58057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9bc7f222c27d8695badee53831e2305c943e58fca76ed7ffee95a51ff4721`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998d611185d7cbaa4fe1b29c4c82e2f5c9b09c8070c2db204e04351d0c79981`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0` - unknown; unknown

```console
$ docker pull docker@sha256:3617129123778bb4c70edbed5f249717569f4ead11ad46b83e4885c3813775e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59faba2e7641334fc344c52dfee2abccbd797367db99d1ffb9e1dde06c5b5c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea82643619a2cc049ccf3cf5ecc7840bffdf522b8052b76245630ef2c73807a`  
		Last Modified: Tue, 11 Nov 2025 06:07:37 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:401d14a2f2adf4049a65a1e43a7015d6535f0a3d9fd3f4983eb2f7b8be34669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133608586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620363b32bc14b7498b2ea91462c609689f37821a91d113ea08c303a429d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0` - unknown; unknown

```console
$ docker pull docker@sha256:05658c0ee5399800317269e821d0af4f2bc594f25082f70dde54d05f1343ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c679cdfbd2c4de098f839b682a1d5ef1ec6a2dd2df6cf57164e9431bb6100a1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a07abadd15bdc841d4aca14903139ea1d3b06379b0c5b04895afc55c44d19c`  
		Last Modified: Tue, 11 Nov 2025 06:07:40 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.0-alpine3.22`

```console
$ docker pull docker@sha256:96789d56621ae702a2f8aa316c87a1a1875dd3f02bf67cdcb56a524a09fa3af9
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

### `docker:29.0.0-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:df7efe7183e533112a8236c5fddb1edf12c96fb2feba3b6b693a285bd7bb993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143957895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cdce60b4d9596765151d2508cad4e3441223cf71e32ba68015def44b654c2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:bf82da9d97fb017eb52fe800bcb19e47f54474e8d981b8682beb615517afd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0164e514b2ea3e21ae8f8c5486cd2d19628d181877991e1232da20933c44b`

```dockerfile
```

-	Layers:
	-	`sha256:d474ac080071d8e06b197e991ae6cd69e0220b949c3e867e07644315c15c39d2`  
		Last Modified: Tue, 11 Nov 2025 06:07:32 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:801cd28b5bdd6f880f7551901af30f6f084bd70c09dffa4ca0d2cace1eba03af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135991944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c369e847de2b33daebebfd4b7581651530f43a5f1705341a2e0fd7e3f1090`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d9e03480f36684f99c499bcac854458fc59fbd5fa1590b2a75308769f18bf`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 7.2 MB (7230266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4413fdb49a4b4c681741a79c06d306c0adce974437e167ab302104c09817f74f`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 89.9 KB (89949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ef3e596708743d134b73dba182acb89d52baa28af431f822db748a0b6e68a7`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84002f98aaa912e73b1fefcb7d1eb964dde81fa74a2ecdb42592b3199151e4a`  
		Last Modified: Tue, 11 Nov 2025 02:10:03 GMT  
		Size: 58.2 MB (58226172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c833c392dc7ac6d8703b1d37c747c18bbb1a7b715d2310cb1714175f258eb28`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefbb114f52aff835ec78ec55484ada326894556ae499be4b38662227429687`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f1c493023b4ed6d738f467fca7f0b2d92b95335adbda5b18bbe15b9af0ccb33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856c1affda75149a5241b1d28d1e6618599f3dbf59e5a63f7405a4307280290e`

```dockerfile
```

-	Layers:
	-	`sha256:e893b3d0edebe68f568f76cf8a8765526bd4f038336efa0e047540a58cc81ece`  
		Last Modified: Tue, 11 Nov 2025 06:07:35 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:0dea739e8da25364ad4b96de17ee4ca9ab3ee4b1853feaeb656908f9c2f15d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134122997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e965328256d5f24c1340bb8fe352992ce0115545213c85811d887055ce2b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:08:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:08:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:08:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:08:57 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231bfd4746adb8d80098ffe2b9e41c38b9b0f3b07364e636f24dfd181f529a3f`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 6.5 MB (6538231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430d5813d2cbd287f1f28c0b9beee442827ab11d4a8ebba2b422df8ab2fdfd5`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 86.4 KB (86387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790a160f5c3b286a104a10316a01fc4f087539c8ef1489b6fce21ad25dbda68c`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac758b28033ab99ed3d93e0a5d7e41217a07d02ff8c0d3a1c23956fdb0fa14`  
		Last Modified: Tue, 11 Nov 2025 02:09:28 GMT  
		Size: 58.1 MB (58057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9bc7f222c27d8695badee53831e2305c943e58fca76ed7ffee95a51ff4721`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998d611185d7cbaa4fe1b29c4c82e2f5c9b09c8070c2db204e04351d0c79981`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:3617129123778bb4c70edbed5f249717569f4ead11ad46b83e4885c3813775e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59faba2e7641334fc344c52dfee2abccbd797367db99d1ffb9e1dde06c5b5c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea82643619a2cc049ccf3cf5ecc7840bffdf522b8052b76245630ef2c73807a`  
		Last Modified: Tue, 11 Nov 2025 06:07:37 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:401d14a2f2adf4049a65a1e43a7015d6535f0a3d9fd3f4983eb2f7b8be34669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133608586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620363b32bc14b7498b2ea91462c609689f37821a91d113ea08c303a429d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:05658c0ee5399800317269e821d0af4f2bc594f25082f70dde54d05f1343ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c679cdfbd2c4de098f839b682a1d5ef1ec6a2dd2df6cf57164e9431bb6100a1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a07abadd15bdc841d4aca14903139ea1d3b06379b0c5b04895afc55c44d19c`  
		Last Modified: Tue, 11 Nov 2025 06:07:40 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.0-cli`

```console
$ docker pull docker@sha256:87858a6dd14149240f4a2c33e0ec0f32a5ac1bb2548c04f5a20694ea25cb6157
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

### `docker:29.0.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:85b69bff6696b21432c9a0c97d9ba577dcfa1abd09c2fe7064521f845db7ba10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74694027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b460f9e12dba9ee2f56aee0f01e5ec9fec819cd562fa6830d4cbe499cb90cfa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:edc7c416b5749e58ae06051f73f58941925ea0e92139cecb3942f82b66548726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ccd16ac07cf0e07f69b5389a4ddc6813b3cc6a9b6e36d4949cb95ac4501849`

```dockerfile
```

-	Layers:
	-	`sha256:a2cc848b3383a4812739dd031cc0bbeb7467ec96000656df5e9cde1d6d3f8633`  
		Last Modified: Tue, 11 Nov 2025 03:07:28 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:db6f1b09c83095931c62c38f3326c38fa50c08aaacfb883ef2690ba2732ba235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70439557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530b79b8ee9c418f2e9616e0ae46c306cbf27d8cef7cd84a6a9833cf7b003dfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8068d2a5a896fd79499397ab7f094ac12aa83ee4089f75aac6336e24e4691bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea34c81a23aa2af2ba356d98981809c05b67bff1ba3c9ea0d5172895744a0bbc`

```dockerfile
```

-	Layers:
	-	`sha256:e5d052648f543fb28f0fe4b56a4b0130450df95ad7ae79e57620bc144564b7f0`  
		Last Modified: Tue, 11 Nov 2025 03:07:31 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4ccec6e40933fa64d0334144f642a1e480f71a6780c4bc3eae361d3eb7cc39e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69434747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b0d5938bdacd4bb4fb88b45fca03668fa50596f84faaca883672554fca777f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:958bb6a5751db20fca83307e98779011066c11405ac2a69e134b82980c08d77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c097d20db918a54283a2ab06f3e60191ce4493c88229975725173c04bc393766`

```dockerfile
```

-	Layers:
	-	`sha256:f788d6efa84036126423fe4369987a8a51132192aed4ccb420682aa9c73fe7b9`  
		Last Modified: Tue, 11 Nov 2025 03:07:33 GMT  
		Size: 38.2 KB (38238 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fb78d3008a96342d542ed9cf971f8d4a833fd1efb7e514b580cb285fba8cf146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69865515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b61bf9d97253c23eb31dc71e0a54e61c41bf2e91d184b357502826e956d7d7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dfc45fa7a7ebd405ac76c818dd144712daa26778ce043a76705b59adadfbf594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89636110a73f7d0bb3efc7ccdf96f43e55da09947af75a3d39f5fc8e01817d7e`

```dockerfile
```

-	Layers:
	-	`sha256:67831bcf8526bf2bbe1929f191e97b780e4ffd6f8c224c78e07320a922349a82`  
		Last Modified: Tue, 11 Nov 2025 03:07:36 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.0-cli-alpine3.22`

```console
$ docker pull docker@sha256:87858a6dd14149240f4a2c33e0ec0f32a5ac1bb2548c04f5a20694ea25cb6157
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

### `docker:29.0.0-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:85b69bff6696b21432c9a0c97d9ba577dcfa1abd09c2fe7064521f845db7ba10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74694027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b460f9e12dba9ee2f56aee0f01e5ec9fec819cd562fa6830d4cbe499cb90cfa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:edc7c416b5749e58ae06051f73f58941925ea0e92139cecb3942f82b66548726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ccd16ac07cf0e07f69b5389a4ddc6813b3cc6a9b6e36d4949cb95ac4501849`

```dockerfile
```

-	Layers:
	-	`sha256:a2cc848b3383a4812739dd031cc0bbeb7467ec96000656df5e9cde1d6d3f8633`  
		Last Modified: Tue, 11 Nov 2025 03:07:28 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:db6f1b09c83095931c62c38f3326c38fa50c08aaacfb883ef2690ba2732ba235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70439557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530b79b8ee9c418f2e9616e0ae46c306cbf27d8cef7cd84a6a9833cf7b003dfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:8068d2a5a896fd79499397ab7f094ac12aa83ee4089f75aac6336e24e4691bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea34c81a23aa2af2ba356d98981809c05b67bff1ba3c9ea0d5172895744a0bbc`

```dockerfile
```

-	Layers:
	-	`sha256:e5d052648f543fb28f0fe4b56a4b0130450df95ad7ae79e57620bc144564b7f0`  
		Last Modified: Tue, 11 Nov 2025 03:07:31 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:4ccec6e40933fa64d0334144f642a1e480f71a6780c4bc3eae361d3eb7cc39e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69434747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b0d5938bdacd4bb4fb88b45fca03668fa50596f84faaca883672554fca777f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:958bb6a5751db20fca83307e98779011066c11405ac2a69e134b82980c08d77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c097d20db918a54283a2ab06f3e60191ce4493c88229975725173c04bc393766`

```dockerfile
```

-	Layers:
	-	`sha256:f788d6efa84036126423fe4369987a8a51132192aed4ccb420682aa9c73fe7b9`  
		Last Modified: Tue, 11 Nov 2025 03:07:33 GMT  
		Size: 38.2 KB (38238 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fb78d3008a96342d542ed9cf971f8d4a833fd1efb7e514b580cb285fba8cf146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69865515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b61bf9d97253c23eb31dc71e0a54e61c41bf2e91d184b357502826e956d7d7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:dfc45fa7a7ebd405ac76c818dd144712daa26778ce043a76705b59adadfbf594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89636110a73f7d0bb3efc7ccdf96f43e55da09947af75a3d39f5fc8e01817d7e`

```dockerfile
```

-	Layers:
	-	`sha256:67831bcf8526bf2bbe1929f191e97b780e4ffd6f8c224c78e07320a922349a82`  
		Last Modified: Tue, 11 Nov 2025 03:07:36 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.0-dind`

```console
$ docker pull docker@sha256:96789d56621ae702a2f8aa316c87a1a1875dd3f02bf67cdcb56a524a09fa3af9
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

### `docker:29.0.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:df7efe7183e533112a8236c5fddb1edf12c96fb2feba3b6b693a285bd7bb993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143957895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cdce60b4d9596765151d2508cad4e3441223cf71e32ba68015def44b654c2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bf82da9d97fb017eb52fe800bcb19e47f54474e8d981b8682beb615517afd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0164e514b2ea3e21ae8f8c5486cd2d19628d181877991e1232da20933c44b`

```dockerfile
```

-	Layers:
	-	`sha256:d474ac080071d8e06b197e991ae6cd69e0220b949c3e867e07644315c15c39d2`  
		Last Modified: Tue, 11 Nov 2025 06:07:32 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:801cd28b5bdd6f880f7551901af30f6f084bd70c09dffa4ca0d2cace1eba03af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135991944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c369e847de2b33daebebfd4b7581651530f43a5f1705341a2e0fd7e3f1090`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d9e03480f36684f99c499bcac854458fc59fbd5fa1590b2a75308769f18bf`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 7.2 MB (7230266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4413fdb49a4b4c681741a79c06d306c0adce974437e167ab302104c09817f74f`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 89.9 KB (89949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ef3e596708743d134b73dba182acb89d52baa28af431f822db748a0b6e68a7`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84002f98aaa912e73b1fefcb7d1eb964dde81fa74a2ecdb42592b3199151e4a`  
		Last Modified: Tue, 11 Nov 2025 02:10:03 GMT  
		Size: 58.2 MB (58226172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c833c392dc7ac6d8703b1d37c747c18bbb1a7b715d2310cb1714175f258eb28`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefbb114f52aff835ec78ec55484ada326894556ae499be4b38662227429687`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f1c493023b4ed6d738f467fca7f0b2d92b95335adbda5b18bbe15b9af0ccb33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856c1affda75149a5241b1d28d1e6618599f3dbf59e5a63f7405a4307280290e`

```dockerfile
```

-	Layers:
	-	`sha256:e893b3d0edebe68f568f76cf8a8765526bd4f038336efa0e047540a58cc81ece`  
		Last Modified: Tue, 11 Nov 2025 06:07:35 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0dea739e8da25364ad4b96de17ee4ca9ab3ee4b1853feaeb656908f9c2f15d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134122997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e965328256d5f24c1340bb8fe352992ce0115545213c85811d887055ce2b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:08:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:08:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:08:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:08:57 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231bfd4746adb8d80098ffe2b9e41c38b9b0f3b07364e636f24dfd181f529a3f`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 6.5 MB (6538231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430d5813d2cbd287f1f28c0b9beee442827ab11d4a8ebba2b422df8ab2fdfd5`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 86.4 KB (86387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790a160f5c3b286a104a10316a01fc4f087539c8ef1489b6fce21ad25dbda68c`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac758b28033ab99ed3d93e0a5d7e41217a07d02ff8c0d3a1c23956fdb0fa14`  
		Last Modified: Tue, 11 Nov 2025 02:09:28 GMT  
		Size: 58.1 MB (58057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9bc7f222c27d8695badee53831e2305c943e58fca76ed7ffee95a51ff4721`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998d611185d7cbaa4fe1b29c4c82e2f5c9b09c8070c2db204e04351d0c79981`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3617129123778bb4c70edbed5f249717569f4ead11ad46b83e4885c3813775e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59faba2e7641334fc344c52dfee2abccbd797367db99d1ffb9e1dde06c5b5c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea82643619a2cc049ccf3cf5ecc7840bffdf522b8052b76245630ef2c73807a`  
		Last Modified: Tue, 11 Nov 2025 06:07:37 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:401d14a2f2adf4049a65a1e43a7015d6535f0a3d9fd3f4983eb2f7b8be34669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133608586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620363b32bc14b7498b2ea91462c609689f37821a91d113ea08c303a429d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:05658c0ee5399800317269e821d0af4f2bc594f25082f70dde54d05f1343ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c679cdfbd2c4de098f839b682a1d5ef1ec6a2dd2df6cf57164e9431bb6100a1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a07abadd15bdc841d4aca14903139ea1d3b06379b0c5b04895afc55c44d19c`  
		Last Modified: Tue, 11 Nov 2025 06:07:40 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.0-dind-alpine3.22`

```console
$ docker pull docker@sha256:96789d56621ae702a2f8aa316c87a1a1875dd3f02bf67cdcb56a524a09fa3af9
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

### `docker:29.0.0-dind-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:df7efe7183e533112a8236c5fddb1edf12c96fb2feba3b6b693a285bd7bb993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143957895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cdce60b4d9596765151d2508cad4e3441223cf71e32ba68015def44b654c2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:bf82da9d97fb017eb52fe800bcb19e47f54474e8d981b8682beb615517afd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0164e514b2ea3e21ae8f8c5486cd2d19628d181877991e1232da20933c44b`

```dockerfile
```

-	Layers:
	-	`sha256:d474ac080071d8e06b197e991ae6cd69e0220b949c3e867e07644315c15c39d2`  
		Last Modified: Tue, 11 Nov 2025 06:07:32 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-dind-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:801cd28b5bdd6f880f7551901af30f6f084bd70c09dffa4ca0d2cace1eba03af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135991944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c369e847de2b33daebebfd4b7581651530f43a5f1705341a2e0fd7e3f1090`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d9e03480f36684f99c499bcac854458fc59fbd5fa1590b2a75308769f18bf`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 7.2 MB (7230266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4413fdb49a4b4c681741a79c06d306c0adce974437e167ab302104c09817f74f`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 89.9 KB (89949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ef3e596708743d134b73dba182acb89d52baa28af431f822db748a0b6e68a7`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84002f98aaa912e73b1fefcb7d1eb964dde81fa74a2ecdb42592b3199151e4a`  
		Last Modified: Tue, 11 Nov 2025 02:10:03 GMT  
		Size: 58.2 MB (58226172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c833c392dc7ac6d8703b1d37c747c18bbb1a7b715d2310cb1714175f258eb28`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefbb114f52aff835ec78ec55484ada326894556ae499be4b38662227429687`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f1c493023b4ed6d738f467fca7f0b2d92b95335adbda5b18bbe15b9af0ccb33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856c1affda75149a5241b1d28d1e6618599f3dbf59e5a63f7405a4307280290e`

```dockerfile
```

-	Layers:
	-	`sha256:e893b3d0edebe68f568f76cf8a8765526bd4f038336efa0e047540a58cc81ece`  
		Last Modified: Tue, 11 Nov 2025 06:07:35 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-dind-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:0dea739e8da25364ad4b96de17ee4ca9ab3ee4b1853feaeb656908f9c2f15d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134122997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e965328256d5f24c1340bb8fe352992ce0115545213c85811d887055ce2b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:08:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:08:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:08:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:08:57 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231bfd4746adb8d80098ffe2b9e41c38b9b0f3b07364e636f24dfd181f529a3f`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 6.5 MB (6538231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430d5813d2cbd287f1f28c0b9beee442827ab11d4a8ebba2b422df8ab2fdfd5`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 86.4 KB (86387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790a160f5c3b286a104a10316a01fc4f087539c8ef1489b6fce21ad25dbda68c`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac758b28033ab99ed3d93e0a5d7e41217a07d02ff8c0d3a1c23956fdb0fa14`  
		Last Modified: Tue, 11 Nov 2025 02:09:28 GMT  
		Size: 58.1 MB (58057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9bc7f222c27d8695badee53831e2305c943e58fca76ed7ffee95a51ff4721`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998d611185d7cbaa4fe1b29c4c82e2f5c9b09c8070c2db204e04351d0c79981`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:3617129123778bb4c70edbed5f249717569f4ead11ad46b83e4885c3813775e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59faba2e7641334fc344c52dfee2abccbd797367db99d1ffb9e1dde06c5b5c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea82643619a2cc049ccf3cf5ecc7840bffdf522b8052b76245630ef2c73807a`  
		Last Modified: Tue, 11 Nov 2025 06:07:37 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-dind-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:401d14a2f2adf4049a65a1e43a7015d6535f0a3d9fd3f4983eb2f7b8be34669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133608586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620363b32bc14b7498b2ea91462c609689f37821a91d113ea08c303a429d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:05658c0ee5399800317269e821d0af4f2bc594f25082f70dde54d05f1343ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c679cdfbd2c4de098f839b682a1d5ef1ec6a2dd2df6cf57164e9431bb6100a1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a07abadd15bdc841d4aca14903139ea1d3b06379b0c5b04895afc55c44d19c`  
		Last Modified: Tue, 11 Nov 2025 06:07:40 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.0-dind-rootless`

```console
$ docker pull docker@sha256:655682420c390d78bdac672dc9d35667fa1e52a760680657f6d45589047602fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.0.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:42ff18328a31c104cd584f80bc4b226cc9758918dcc508665d6a1b95db855471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164727869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6546ea708bf60ea1e4ef3695c1216d35872e9d7c0b0e22ad42fe24c8875d78c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
# Tue, 11 Nov 2025 03:10:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 11 Nov 2025 03:10:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 11 Nov 2025 03:10:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 11 Nov 2025 03:10:11 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafcd68783d7705964732be0808bd0bb79510ff08a912dbafcc3fd7a22fb6cde`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 3.4 MB (3398393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877c138ce4f7a03c272f7263704eed9984e712511333124d8573865dcc29fc19`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f6919cf3ae19fe242e3ae3e2e69ba5fdad9b62ee1ba25e00d02f9ab008d2e8`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64635a629124d1d8a7e1ae88ae288f18e1979a129293587b291dffd3e2262bf0`  
		Last Modified: Tue, 11 Nov 2025 03:10:28 GMT  
		Size: 17.4 MB (17370240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ee1e48d6f34d4967b6e2533d92965d2ce3d9cb76988f11587335211d8dc6a4`  
		Last Modified: Tue, 11 Nov 2025 03:10:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ab78b124a9ff0ce7253385fe42b866700df87ec72d0c74762409d5a09fe1441d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3774ad7d79781a69ae44de5f03cba5564f606f9c9cbfe569307486299cd910`

```dockerfile
```

-	Layers:
	-	`sha256:0067f650317a33b012070bdb14ddb432839900e99f3ed8642730f12baf986d52`  
		Last Modified: Tue, 11 Nov 2025 06:07:46 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ea7d11c209f5f9c6c6b0299573681a3ad6032cbcbf24d22fbf8bf913961591db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154706892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb198c77d75eea1b7edffcac43925972fa2a02d4280a799c54cb052f39ed2229`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
# Tue, 11 Nov 2025 03:09:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 11 Nov 2025 03:09:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 11 Nov 2025 03:09:52 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 11 Nov 2025 03:09:53 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcb06fab37a52d9a24735f766783d73c09eb40a62c6b55aad8e566ab5cc722c`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 3.4 MB (3389934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264ee650ea75362a13bdaaf8fde957d1a108659352e29da95c8e5b9068bbee38`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca921cac3d58424a9d678c45dc156d4979e295b0b8bcc70b563adaf098d26484`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3eeaf9a370146e91d691c000c720b150c79437f704b1f1a2ad15fb331dff742`  
		Last Modified: Tue, 11 Nov 2025 03:10:12 GMT  
		Size: 17.7 MB (17707031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e43df59a31a48918f41ad14da8cca78b0b51f4d960b632a4e97f489ba38a45`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c09f760ea44c49943c419da5b2673f21ffbb51a0aff0fdd1e846779a8799a600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e8551cb7c3cdaf5e80a2b47160a8c65c3d4ed6d7db3b6e82aebd9e41281bf1`

```dockerfile
```

-	Layers:
	-	`sha256:3033c8a433fb48e4ad4962e0385738ce667cdb9d654449c9c648c59dd437e1d5`  
		Last Modified: Tue, 11 Nov 2025 06:07:49 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.0-windowsservercore`

```console
$ docker pull docker@sha256:72d299112395e5cec5a7ae09c7e757b1c70362702ec37656206b365f8e81580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `docker:29.0.0-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:d3430dae25034c55c56dd585271ca3ff7633e012a1ba11f1498b04f25693ef2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3286034630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d734e887c89ba0c951f704dfa1208365d6a2457d51ed341c05d8223c37bd652a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Tue, 11 Nov 2025 01:09:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:09:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:09:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:09:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:09:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:09:59 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:10:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:10:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:10:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cbb13e31831b4a401483474d0b3761d526123e4940ffefb9e59ca0b95bd928`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11778e4fa17626dc91d9d9cb467403166f0cc6134bcadc2c6c394c23f4f77350`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 385.3 KB (385346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea88d46cd119b0ed069843b33c117aa143e9f6c36695cf17ee648d8dcf3655b`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa5fa37b5931fe92505e086ba67d6dfb0da4ae0172b58b04d5bb013277f60b9`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ada5899e6769690fd204f9f137706c9612fa97a65835249036bb92593e5eb`  
		Last Modified: Tue, 11 Nov 2025 01:19:20 GMT  
		Size: 19.4 MB (19430246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0272441663d6fec957c0b4d34b58b8a19b8808f1771c45d4c591dff46cb951`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918e1ab8b826581917ab7b2d53b2c6a5f2b06ce5c03f208c14dea008b3cfe60`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce36d1376a231ae8f91e59637fe876b6fa19bccb1bfd0a4e96c4d2b5d24a5ae5`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f749f808cf8c30f6a915e56d9393b185ef4a06c9ab0ce38fab25952828f43c6d`  
		Last Modified: Tue, 11 Nov 2025 01:19:18 GMT  
		Size: 23.2 MB (23173614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4c6efb8d391dc41567c8e29c5f2c1aaa0d6372c5dab092454b25133fbaf22`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f789efcc4cd75dab1e0486cceffa4fbb47564e174bfb011d328003e81c690ad`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73f4b7bd98ba3e36992613125ce4ea0186486089e65bd5b3be8e14604b916f0`  
		Last Modified: Tue, 11 Nov 2025 01:19:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ae4ce13bc5f392ee40f76f48ccf05ef5a576bd04b4b7affecfadde7443a36`  
		Last Modified: Tue, 11 Nov 2025 01:19:22 GMT  
		Size: 22.7 MB (22686606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.0.0-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:4da74ebb24ba1ed05d837769e2868b3fced76e9d625b5033e5c6bd554dba5b1c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1642975859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b248f8970d471ca71d2fe5d8cf5a618741a9ae195807e67894fa707304be22f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Tue, 11 Nov 2025 01:31:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:32:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:32:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:32:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:33:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:08 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:33:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:33:10 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:33:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:33:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607358d94499b322187d8294abffa374df336a542ba3a7746e54550a559a84e3`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff233fc8be81f08e0fd27b16161e9cb9e883edbeeb55293e4f90cf045577ee6b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 510.8 KB (510798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5647cb091467ce953f8492c583014320a568592f5d1f5685de40d7c64f5e5fe8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45373dae92aa5007d34f749e78b0e5899e1a7c3c1ce4329315c3a5d7969c469b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cffa7afe37dfd330f9aa05e82a6f05a309d0d2079e615fcab933f7b9ead0d7`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 19.4 MB (19419747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f4ab1b20e761366e4592a4a695a67d6fb6ad55c780094fad9976df3ebeb21`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477c725c69905fa95c18552eb154560a212870c86cb468c7570ef9beea16e8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade21b9c6cec037cb7d2f205612a41a75789f0857a3304753e001984561e9983`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7311ebb09d47c704ac9a5d171113840b634120dc0c680eb276a91ddee2efd`  
		Last Modified: Tue, 11 Nov 2025 01:44:35 GMT  
		Size: 23.2 MB (23163257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28603a23c96e1bd9ba9ee0b8e4c446e6e01e8f268c3b8a292c4b7749184649d5`  
		Last Modified: Tue, 11 Nov 2025 01:44:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e94373564db23e5d8ea9cc012d861df363325d542c9908aee4273fe0a84566`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c07acbdd0f1cc9183784756376bc05490f3e9257490fc0a387eceb8ff38c645`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be490461e18aba4834222d552c012a6093108c1e590650b34829a457e978bc8c`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 22.7 MB (22677281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9c96d3736d1657483916877049c0ccbdb057a8df315fcb3e663048acfbd132d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `docker:29.0.0-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:4da74ebb24ba1ed05d837769e2868b3fced76e9d625b5033e5c6bd554dba5b1c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1642975859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b248f8970d471ca71d2fe5d8cf5a618741a9ae195807e67894fa707304be22f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Tue, 11 Nov 2025 01:31:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:32:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:32:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:32:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:33:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:08 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:33:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:33:10 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:33:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:33:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607358d94499b322187d8294abffa374df336a542ba3a7746e54550a559a84e3`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff233fc8be81f08e0fd27b16161e9cb9e883edbeeb55293e4f90cf045577ee6b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 510.8 KB (510798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5647cb091467ce953f8492c583014320a568592f5d1f5685de40d7c64f5e5fe8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45373dae92aa5007d34f749e78b0e5899e1a7c3c1ce4329315c3a5d7969c469b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cffa7afe37dfd330f9aa05e82a6f05a309d0d2079e615fcab933f7b9ead0d7`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 19.4 MB (19419747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f4ab1b20e761366e4592a4a695a67d6fb6ad55c780094fad9976df3ebeb21`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477c725c69905fa95c18552eb154560a212870c86cb468c7570ef9beea16e8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade21b9c6cec037cb7d2f205612a41a75789f0857a3304753e001984561e9983`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7311ebb09d47c704ac9a5d171113840b634120dc0c680eb276a91ddee2efd`  
		Last Modified: Tue, 11 Nov 2025 01:44:35 GMT  
		Size: 23.2 MB (23163257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28603a23c96e1bd9ba9ee0b8e4c446e6e01e8f268c3b8a292c4b7749184649d5`  
		Last Modified: Tue, 11 Nov 2025 01:44:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e94373564db23e5d8ea9cc012d861df363325d542c9908aee4273fe0a84566`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c07acbdd0f1cc9183784756376bc05490f3e9257490fc0a387eceb8ff38c645`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be490461e18aba4834222d552c012a6093108c1e590650b34829a457e978bc8c`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 22.7 MB (22677281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:cf52fc75c50a0b3ee0fd34f484cb9e7aa12c6b6f6187e520f1fc9cb2a96807fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `docker:29.0.0-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:d3430dae25034c55c56dd585271ca3ff7633e012a1ba11f1498b04f25693ef2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3286034630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d734e887c89ba0c951f704dfa1208365d6a2457d51ed341c05d8223c37bd652a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Tue, 11 Nov 2025 01:09:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:09:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:09:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:09:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:09:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:09:59 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:10:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:10:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:10:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cbb13e31831b4a401483474d0b3761d526123e4940ffefb9e59ca0b95bd928`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11778e4fa17626dc91d9d9cb467403166f0cc6134bcadc2c6c394c23f4f77350`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 385.3 KB (385346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea88d46cd119b0ed069843b33c117aa143e9f6c36695cf17ee648d8dcf3655b`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa5fa37b5931fe92505e086ba67d6dfb0da4ae0172b58b04d5bb013277f60b9`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ada5899e6769690fd204f9f137706c9612fa97a65835249036bb92593e5eb`  
		Last Modified: Tue, 11 Nov 2025 01:19:20 GMT  
		Size: 19.4 MB (19430246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0272441663d6fec957c0b4d34b58b8a19b8808f1771c45d4c591dff46cb951`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918e1ab8b826581917ab7b2d53b2c6a5f2b06ce5c03f208c14dea008b3cfe60`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce36d1376a231ae8f91e59637fe876b6fa19bccb1bfd0a4e96c4d2b5d24a5ae5`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f749f808cf8c30f6a915e56d9393b185ef4a06c9ab0ce38fab25952828f43c6d`  
		Last Modified: Tue, 11 Nov 2025 01:19:18 GMT  
		Size: 23.2 MB (23173614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4c6efb8d391dc41567c8e29c5f2c1aaa0d6372c5dab092454b25133fbaf22`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f789efcc4cd75dab1e0486cceffa4fbb47564e174bfb011d328003e81c690ad`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73f4b7bd98ba3e36992613125ce4ea0186486089e65bd5b3be8e14604b916f0`  
		Last Modified: Tue, 11 Nov 2025 01:19:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ae4ce13bc5f392ee40f76f48ccf05ef5a576bd04b4b7affecfadde7443a36`  
		Last Modified: Tue, 11 Nov 2025 01:19:22 GMT  
		Size: 22.7 MB (22686606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:87858a6dd14149240f4a2c33e0ec0f32a5ac1bb2548c04f5a20694ea25cb6157
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
$ docker pull docker@sha256:85b69bff6696b21432c9a0c97d9ba577dcfa1abd09c2fe7064521f845db7ba10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74694027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b460f9e12dba9ee2f56aee0f01e5ec9fec819cd562fa6830d4cbe499cb90cfa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:edc7c416b5749e58ae06051f73f58941925ea0e92139cecb3942f82b66548726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ccd16ac07cf0e07f69b5389a4ddc6813b3cc6a9b6e36d4949cb95ac4501849`

```dockerfile
```

-	Layers:
	-	`sha256:a2cc848b3383a4812739dd031cc0bbeb7467ec96000656df5e9cde1d6d3f8633`  
		Last Modified: Tue, 11 Nov 2025 03:07:28 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:db6f1b09c83095931c62c38f3326c38fa50c08aaacfb883ef2690ba2732ba235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70439557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530b79b8ee9c418f2e9616e0ae46c306cbf27d8cef7cd84a6a9833cf7b003dfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:8068d2a5a896fd79499397ab7f094ac12aa83ee4089f75aac6336e24e4691bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea34c81a23aa2af2ba356d98981809c05b67bff1ba3c9ea0d5172895744a0bbc`

```dockerfile
```

-	Layers:
	-	`sha256:e5d052648f543fb28f0fe4b56a4b0130450df95ad7ae79e57620bc144564b7f0`  
		Last Modified: Tue, 11 Nov 2025 03:07:31 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4ccec6e40933fa64d0334144f642a1e480f71a6780c4bc3eae361d3eb7cc39e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69434747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b0d5938bdacd4bb4fb88b45fca03668fa50596f84faaca883672554fca777f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:958bb6a5751db20fca83307e98779011066c11405ac2a69e134b82980c08d77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c097d20db918a54283a2ab06f3e60191ce4493c88229975725173c04bc393766`

```dockerfile
```

-	Layers:
	-	`sha256:f788d6efa84036126423fe4369987a8a51132192aed4ccb420682aa9c73fe7b9`  
		Last Modified: Tue, 11 Nov 2025 03:07:33 GMT  
		Size: 38.2 KB (38238 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fb78d3008a96342d542ed9cf971f8d4a833fd1efb7e514b580cb285fba8cf146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69865515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b61bf9d97253c23eb31dc71e0a54e61c41bf2e91d184b357502826e956d7d7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:dfc45fa7a7ebd405ac76c818dd144712daa26778ce043a76705b59adadfbf594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89636110a73f7d0bb3efc7ccdf96f43e55da09947af75a3d39f5fc8e01817d7e`

```dockerfile
```

-	Layers:
	-	`sha256:67831bcf8526bf2bbe1929f191e97b780e4ffd6f8c224c78e07320a922349a82`  
		Last Modified: Tue, 11 Nov 2025 03:07:36 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:96789d56621ae702a2f8aa316c87a1a1875dd3f02bf67cdcb56a524a09fa3af9
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
$ docker pull docker@sha256:df7efe7183e533112a8236c5fddb1edf12c96fb2feba3b6b693a285bd7bb993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143957895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cdce60b4d9596765151d2508cad4e3441223cf71e32ba68015def44b654c2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:bf82da9d97fb017eb52fe800bcb19e47f54474e8d981b8682beb615517afd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0164e514b2ea3e21ae8f8c5486cd2d19628d181877991e1232da20933c44b`

```dockerfile
```

-	Layers:
	-	`sha256:d474ac080071d8e06b197e991ae6cd69e0220b949c3e867e07644315c15c39d2`  
		Last Modified: Tue, 11 Nov 2025 06:07:32 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:801cd28b5bdd6f880f7551901af30f6f084bd70c09dffa4ca0d2cace1eba03af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135991944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c369e847de2b33daebebfd4b7581651530f43a5f1705341a2e0fd7e3f1090`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d9e03480f36684f99c499bcac854458fc59fbd5fa1590b2a75308769f18bf`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 7.2 MB (7230266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4413fdb49a4b4c681741a79c06d306c0adce974437e167ab302104c09817f74f`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 89.9 KB (89949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ef3e596708743d134b73dba182acb89d52baa28af431f822db748a0b6e68a7`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84002f98aaa912e73b1fefcb7d1eb964dde81fa74a2ecdb42592b3199151e4a`  
		Last Modified: Tue, 11 Nov 2025 02:10:03 GMT  
		Size: 58.2 MB (58226172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c833c392dc7ac6d8703b1d37c747c18bbb1a7b715d2310cb1714175f258eb28`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefbb114f52aff835ec78ec55484ada326894556ae499be4b38662227429687`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:f1c493023b4ed6d738f467fca7f0b2d92b95335adbda5b18bbe15b9af0ccb33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856c1affda75149a5241b1d28d1e6618599f3dbf59e5a63f7405a4307280290e`

```dockerfile
```

-	Layers:
	-	`sha256:e893b3d0edebe68f568f76cf8a8765526bd4f038336efa0e047540a58cc81ece`  
		Last Modified: Tue, 11 Nov 2025 06:07:35 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0dea739e8da25364ad4b96de17ee4ca9ab3ee4b1853feaeb656908f9c2f15d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134122997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e965328256d5f24c1340bb8fe352992ce0115545213c85811d887055ce2b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:08:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:08:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:08:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:08:57 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231bfd4746adb8d80098ffe2b9e41c38b9b0f3b07364e636f24dfd181f529a3f`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 6.5 MB (6538231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430d5813d2cbd287f1f28c0b9beee442827ab11d4a8ebba2b422df8ab2fdfd5`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 86.4 KB (86387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790a160f5c3b286a104a10316a01fc4f087539c8ef1489b6fce21ad25dbda68c`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac758b28033ab99ed3d93e0a5d7e41217a07d02ff8c0d3a1c23956fdb0fa14`  
		Last Modified: Tue, 11 Nov 2025 02:09:28 GMT  
		Size: 58.1 MB (58057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9bc7f222c27d8695badee53831e2305c943e58fca76ed7ffee95a51ff4721`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998d611185d7cbaa4fe1b29c4c82e2f5c9b09c8070c2db204e04351d0c79981`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:3617129123778bb4c70edbed5f249717569f4ead11ad46b83e4885c3813775e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59faba2e7641334fc344c52dfee2abccbd797367db99d1ffb9e1dde06c5b5c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea82643619a2cc049ccf3cf5ecc7840bffdf522b8052b76245630ef2c73807a`  
		Last Modified: Tue, 11 Nov 2025 06:07:37 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:401d14a2f2adf4049a65a1e43a7015d6535f0a3d9fd3f4983eb2f7b8be34669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133608586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620363b32bc14b7498b2ea91462c609689f37821a91d113ea08c303a429d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:05658c0ee5399800317269e821d0af4f2bc594f25082f70dde54d05f1343ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c679cdfbd2c4de098f839b682a1d5ef1ec6a2dd2df6cf57164e9431bb6100a1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a07abadd15bdc841d4aca14903139ea1d3b06379b0c5b04895afc55c44d19c`  
		Last Modified: Tue, 11 Nov 2025 06:07:40 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:655682420c390d78bdac672dc9d35667fa1e52a760680657f6d45589047602fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:42ff18328a31c104cd584f80bc4b226cc9758918dcc508665d6a1b95db855471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164727869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6546ea708bf60ea1e4ef3695c1216d35872e9d7c0b0e22ad42fe24c8875d78c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
# Tue, 11 Nov 2025 03:10:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 11 Nov 2025 03:10:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 11 Nov 2025 03:10:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 11 Nov 2025 03:10:11 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 11 Nov 2025 03:10:11 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafcd68783d7705964732be0808bd0bb79510ff08a912dbafcc3fd7a22fb6cde`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 3.4 MB (3398393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877c138ce4f7a03c272f7263704eed9984e712511333124d8573865dcc29fc19`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f6919cf3ae19fe242e3ae3e2e69ba5fdad9b62ee1ba25e00d02f9ab008d2e8`  
		Last Modified: Tue, 11 Nov 2025 03:10:26 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64635a629124d1d8a7e1ae88ae288f18e1979a129293587b291dffd3e2262bf0`  
		Last Modified: Tue, 11 Nov 2025 03:10:28 GMT  
		Size: 17.4 MB (17370240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ee1e48d6f34d4967b6e2533d92965d2ce3d9cb76988f11587335211d8dc6a4`  
		Last Modified: Tue, 11 Nov 2025 03:10:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ab78b124a9ff0ce7253385fe42b866700df87ec72d0c74762409d5a09fe1441d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3774ad7d79781a69ae44de5f03cba5564f606f9c9cbfe569307486299cd910`

```dockerfile
```

-	Layers:
	-	`sha256:0067f650317a33b012070bdb14ddb432839900e99f3ed8642730f12baf986d52`  
		Last Modified: Tue, 11 Nov 2025 06:07:46 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ea7d11c209f5f9c6c6b0299573681a3ad6032cbcbf24d22fbf8bf913961591db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154706892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb198c77d75eea1b7edffcac43925972fa2a02d4280a799c54cb052f39ed2229`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
# Tue, 11 Nov 2025 03:09:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 11 Nov 2025 03:09:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 11 Nov 2025 03:09:52 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 11 Nov 2025 03:09:53 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 11 Nov 2025 03:09:53 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcb06fab37a52d9a24735f766783d73c09eb40a62c6b55aad8e566ab5cc722c`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 3.4 MB (3389934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264ee650ea75362a13bdaaf8fde957d1a108659352e29da95c8e5b9068bbee38`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca921cac3d58424a9d678c45dc156d4979e295b0b8bcc70b563adaf098d26484`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3eeaf9a370146e91d691c000c720b150c79437f704b1f1a2ad15fb331dff742`  
		Last Modified: Tue, 11 Nov 2025 03:10:12 GMT  
		Size: 17.7 MB (17707031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e43df59a31a48918f41ad14da8cca78b0b51f4d960b632a4e97f489ba38a45`  
		Last Modified: Tue, 11 Nov 2025 03:10:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c09f760ea44c49943c419da5b2673f21ffbb51a0aff0fdd1e846779a8799a600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e8551cb7c3cdaf5e80a2b47160a8c65c3d4ed6d7db3b6e82aebd9e41281bf1`

```dockerfile
```

-	Layers:
	-	`sha256:3033c8a433fb48e4ad4962e0385738ce667cdb9d654449c9c648c59dd437e1d5`  
		Last Modified: Tue, 11 Nov 2025 06:07:49 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:96789d56621ae702a2f8aa316c87a1a1875dd3f02bf67cdcb56a524a09fa3af9
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
$ docker pull docker@sha256:df7efe7183e533112a8236c5fddb1edf12c96fb2feba3b6b693a285bd7bb993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143957895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cdce60b4d9596765151d2508cad4e3441223cf71e32ba68015def44b654c2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:55 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:57 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:10:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:10:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:10:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:10:05 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:10:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:10:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:10:05 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fabf041875547d8eea03dd31be61a6d1f3f84777d0ac1e1b201c38f5cc88cec`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 8.2 MB (8232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b686ba714808a7fb2327423944a089686810e171ce650a32fae21b58abd842`  
		Last Modified: Tue, 11 Nov 2025 01:09:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cebff0d0f2ed964836dcf5b3424704976b60ee7613926128c99359ca770516`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 18.8 MB (18754494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c01cfc9bebac0ec1d958067a1a9f6ae290e55fa0bd78fba495ecbc43a1bcdd`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 22.2 MB (22158440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8c41a7eb781651e66dee3bbc02cc1f790337c4a6225097aac62e3a1bfe0de`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e915762d7ff9b62eaad013d0abbafa71e75a7d1152d8545f68fa4c6ec5f4e`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ec461ec05e887cfa1cc39a7a3a4c85fbee74e24a76a9020661312db1a9ce8`  
		Last Modified: Tue, 11 Nov 2025 01:09:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44badd7f13bf5ccfed61b7b62d1ec8d36f1a9d9066678f94dde8a847118bda9f`  
		Last Modified: Tue, 11 Nov 2025 01:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a2fcdfe0c6b3921f94239104a6eb594ed4d3179229cbb7dc6f90ae8db33f3`  
		Last Modified: Tue, 11 Nov 2025 02:10:23 GMT  
		Size: 6.9 MB (6905420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5e833d4712b4ef973fdb06b79242b5f02bf49fc586c97c7e2138db0bb637f`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 90.4 KB (90390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360da3ffb1ace3d451ed5e0d9fc671f2c9cf740ed5a1389ddfa8e28e4e4f70ec`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08d143fa33203fabc0409b1629ced9646f0a4c1af02793d20ad9e2478eeb64`  
		Last Modified: Tue, 11 Nov 2025 02:10:33 GMT  
		Size: 62.3 MB (62262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf78bc19f9bd63263aaf35a3dacaf84e0ec34fb5e22174166775add4e741697`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e494ff47a785f361086fc0bdff6b108999a81295fda0bdb9f6a78fc9add5d54`  
		Last Modified: Tue, 11 Nov 2025 02:10:22 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:bf82da9d97fb017eb52fe800bcb19e47f54474e8d981b8682beb615517afd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0164e514b2ea3e21ae8f8c5486cd2d19628d181877991e1232da20933c44b`

```dockerfile
```

-	Layers:
	-	`sha256:d474ac080071d8e06b197e991ae6cd69e0220b949c3e867e07644315c15c39d2`  
		Last Modified: Tue, 11 Nov 2025 06:07:32 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:801cd28b5bdd6f880f7551901af30f6f084bd70c09dffa4ca0d2cace1eba03af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135991944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c369e847de2b33daebebfd4b7581651530f43a5f1705341a2e0fd7e3f1090`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:41 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:42 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1a0fc715ea53e10f2815e09776862a581c4ce009a1b6ae466ee406071261`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 8.1 MB (8140524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb61f26b1280442ef80f26cbfc7b06a4ed30512f986b45491d6bf8075e3294`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324561800fd38e95059980e7ded048583bf417e09d980ccefca6040404b7d4b`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 17.6 MB (17554109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d38300265819a53530640e35b7d0c87f1b6e07ac22f1f83fab1ac0092cc5a`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.8 MB (20758318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc21cdf2b5470978c83c8f2178f414b7feb4ad5d25298b5d8419e8cee91ca63`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 20.5 MB (20480370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bf76636d5d7f62ae80c72d676a5691d3971338009bf7b82017c872ecc91c5`  
		Last Modified: Tue, 11 Nov 2025 01:08:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0879151c63650636ca1fde021a79d0b47092a5531080a3e1df68cb18d50cf`  
		Last Modified: Tue, 11 Nov 2025 01:08:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92921641a3b5dade6bda2d363d294411b22aeb315cb5af83aa5428798d585c`  
		Last Modified: Tue, 11 Nov 2025 01:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d9e03480f36684f99c499bcac854458fc59fbd5fa1590b2a75308769f18bf`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 7.2 MB (7230266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4413fdb49a4b4c681741a79c06d306c0adce974437e167ab302104c09817f74f`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 89.9 KB (89949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ef3e596708743d134b73dba182acb89d52baa28af431f822db748a0b6e68a7`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84002f98aaa912e73b1fefcb7d1eb964dde81fa74a2ecdb42592b3199151e4a`  
		Last Modified: Tue, 11 Nov 2025 02:10:03 GMT  
		Size: 58.2 MB (58226172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c833c392dc7ac6d8703b1d37c747c18bbb1a7b715d2310cb1714175f258eb28`  
		Last Modified: Tue, 11 Nov 2025 02:09:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefbb114f52aff835ec78ec55484ada326894556ae499be4b38662227429687`  
		Last Modified: Tue, 11 Nov 2025 02:09:59 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:f1c493023b4ed6d738f467fca7f0b2d92b95335adbda5b18bbe15b9af0ccb33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856c1affda75149a5241b1d28d1e6618599f3dbf59e5a63f7405a4307280290e`

```dockerfile
```

-	Layers:
	-	`sha256:e893b3d0edebe68f568f76cf8a8765526bd4f038336efa0e047540a58cc81ece`  
		Last Modified: Tue, 11 Nov 2025 06:07:35 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:0dea739e8da25364ad4b96de17ee4ca9ab3ee4b1853feaeb656908f9c2f15d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134122997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e965328256d5f24c1340bb8fe352992ce0115545213c85811d887055ce2b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:44 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:08:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:08:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:08:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:08:57 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:08:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:08:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:08:57 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e04557caeb7fadb3fbba7c0c5ea531a2e7af004726814ebbf3f62f50c43fd`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 7.5 MB (7461404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd13fa9bf27e06232748f36d0168ac1542282e9810e74a2601fcefbc7a9bcd`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84a5a4bbafb638b50bac7853474d5fe82bb4e2323f3468ddfd45ee461854ca`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 17.5 MB (17542458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff6d2fe5a75b3ce398950dd3d391723862ba199e9d99bc85b84c4be1cf7d6a`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 20.7 MB (20744401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ab7d670d8d3bcd1841dc27cca873dd82379539a78c940711ac1b5ccc4819a`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 20.5 MB (20462774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11356e62fd49a596c18fda01294366fc06170217c69ff05c1d7d1e202be0f1ea`  
		Last Modified: Tue, 11 Nov 2025 01:09:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06eb112e5a671c1bdbe33554670ebed014ad81b8c14c29bf2cf2c1115b287d`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614f6cdaff1f2640039cc1b952e437158372dd7117f46d934348c3c97d69ed`  
		Last Modified: Tue, 11 Nov 2025 01:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231bfd4746adb8d80098ffe2b9e41c38b9b0f3b07364e636f24dfd181f529a3f`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 6.5 MB (6538231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430d5813d2cbd287f1f28c0b9beee442827ab11d4a8ebba2b422df8ab2fdfd5`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 86.4 KB (86387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790a160f5c3b286a104a10316a01fc4f087539c8ef1489b6fce21ad25dbda68c`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac758b28033ab99ed3d93e0a5d7e41217a07d02ff8c0d3a1c23956fdb0fa14`  
		Last Modified: Tue, 11 Nov 2025 02:09:28 GMT  
		Size: 58.1 MB (58057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9bc7f222c27d8695badee53831e2305c943e58fca76ed7ffee95a51ff4721`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998d611185d7cbaa4fe1b29c4c82e2f5c9b09c8070c2db204e04351d0c79981`  
		Last Modified: Tue, 11 Nov 2025 02:09:24 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:3617129123778bb4c70edbed5f249717569f4ead11ad46b83e4885c3813775e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59faba2e7641334fc344c52dfee2abccbd797367db99d1ffb9e1dde06c5b5c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea82643619a2cc049ccf3cf5ecc7840bffdf522b8052b76245630ef2c73807a`  
		Last Modified: Tue, 11 Nov 2025 06:07:37 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:401d14a2f2adf4049a65a1e43a7015d6535f0a3d9fd3f4983eb2f7b8be34669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133608586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620363b32bc14b7498b2ea91462c609689f37821a91d113ea08c303a429d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 01:08:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Nov 2025 01:08:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:08:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Nov 2025 01:08:16 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:08:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Nov 2025 01:08:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:08:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Nov 2025 01:08:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Nov 2025 01:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 01:08:18 GMT
CMD ["sh"]
# Tue, 11 Nov 2025 02:09:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 11 Nov 2025 02:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 11 Nov 2025 02:09:54 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 11 Nov 2025 02:09:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 02:09:55 GMT
VOLUME [/var/lib/docker]
# Tue, 11 Nov 2025 02:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 11 Nov 2025 02:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 11 Nov 2025 02:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577a6012f7667bff575ea0ef292bf885801c6b7ab732f476adfb91dc25229ce`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 8.3 MB (8257275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ed861d72539c0099aeb49c5a9d5bc5b4de0498ed01553845d0b3f87b1041`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbeeb19fca5892fc66104cae712fbc6cf0bab79caced904b1cd910ae9b5f29e`  
		Last Modified: Tue, 11 Nov 2025 01:08:34 GMT  
		Size: 17.3 MB (17324735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8aa260c1963b0b8a977e9aecc353c5312a45bdc10e8f6827a8256bee6be96`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 20.3 MB (20273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848ec545ca4de1fe1bc655bbe67e69aca3a003d658b47655315f9560962a18`  
		Last Modified: Tue, 11 Nov 2025 01:08:35 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980a95195ac972a8a18c2406cce5bffdfb08974f7347d710d9ed1ed0dddeac`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a3898f9b4c34994e5c6afdadb0d6a9e73981b0f8970b6c3527ae182040be`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86593df46054c25fa73ff275fbe5b997b84895b23e43c969bed89cb89dcbb07c`  
		Last Modified: Tue, 11 Nov 2025 01:08:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a66f35cde104c107d31e04ffe08d38ccebeb642862b18099524d8059b3353d`  
		Last Modified: Tue, 11 Nov 2025 02:10:12 GMT  
		Size: 7.1 MB (7140840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd6acb76abc9303f1488db2cbe028230115513cf76b3b86b360237f55415870`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 99.5 KB (99503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045268a2d24bc88b09172bccad1df7236726ef53deac768324c86f8545244e`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9032ab73d8b1079b0a0ddc572862152765c60e979fb95b1acf71d42d71179`  
		Last Modified: Tue, 11 Nov 2025 02:10:16 GMT  
		Size: 56.5 MB (56496727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086b7c274fef2009defc7acd65543c548fdbde5f325687df1f5e9c3869ec019`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044258420b8bb73680c9f02742e91ddd83fc82ef05d76ccd8a2bfb507708d845`  
		Last Modified: Tue, 11 Nov 2025 02:10:11 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:05658c0ee5399800317269e821d0af4f2bc594f25082f70dde54d05f1343ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c679cdfbd2c4de098f839b682a1d5ef1ec6a2dd2df6cf57164e9431bb6100a1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a07abadd15bdc841d4aca14903139ea1d3b06379b0c5b04895afc55c44d19c`  
		Last Modified: Tue, 11 Nov 2025 06:07:40 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:72d299112395e5cec5a7ae09c7e757b1c70362702ec37656206b365f8e81580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `docker:windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:d3430dae25034c55c56dd585271ca3ff7633e012a1ba11f1498b04f25693ef2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3286034630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d734e887c89ba0c951f704dfa1208365d6a2457d51ed341c05d8223c37bd652a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Tue, 11 Nov 2025 01:09:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:09:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:09:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:09:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:09:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:09:59 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:10:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:10:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:10:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cbb13e31831b4a401483474d0b3761d526123e4940ffefb9e59ca0b95bd928`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11778e4fa17626dc91d9d9cb467403166f0cc6134bcadc2c6c394c23f4f77350`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 385.3 KB (385346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea88d46cd119b0ed069843b33c117aa143e9f6c36695cf17ee648d8dcf3655b`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa5fa37b5931fe92505e086ba67d6dfb0da4ae0172b58b04d5bb013277f60b9`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ada5899e6769690fd204f9f137706c9612fa97a65835249036bb92593e5eb`  
		Last Modified: Tue, 11 Nov 2025 01:19:20 GMT  
		Size: 19.4 MB (19430246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0272441663d6fec957c0b4d34b58b8a19b8808f1771c45d4c591dff46cb951`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918e1ab8b826581917ab7b2d53b2c6a5f2b06ce5c03f208c14dea008b3cfe60`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce36d1376a231ae8f91e59637fe876b6fa19bccb1bfd0a4e96c4d2b5d24a5ae5`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f749f808cf8c30f6a915e56d9393b185ef4a06c9ab0ce38fab25952828f43c6d`  
		Last Modified: Tue, 11 Nov 2025 01:19:18 GMT  
		Size: 23.2 MB (23173614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4c6efb8d391dc41567c8e29c5f2c1aaa0d6372c5dab092454b25133fbaf22`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f789efcc4cd75dab1e0486cceffa4fbb47564e174bfb011d328003e81c690ad`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73f4b7bd98ba3e36992613125ce4ea0186486089e65bd5b3be8e14604b916f0`  
		Last Modified: Tue, 11 Nov 2025 01:19:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ae4ce13bc5f392ee40f76f48ccf05ef5a576bd04b4b7affecfadde7443a36`  
		Last Modified: Tue, 11 Nov 2025 01:19:22 GMT  
		Size: 22.7 MB (22686606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:4da74ebb24ba1ed05d837769e2868b3fced76e9d625b5033e5c6bd554dba5b1c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1642975859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b248f8970d471ca71d2fe5d8cf5a618741a9ae195807e67894fa707304be22f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Tue, 11 Nov 2025 01:31:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:32:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:32:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:32:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:33:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:08 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:33:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:33:10 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:33:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:33:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607358d94499b322187d8294abffa374df336a542ba3a7746e54550a559a84e3`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff233fc8be81f08e0fd27b16161e9cb9e883edbeeb55293e4f90cf045577ee6b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 510.8 KB (510798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5647cb091467ce953f8492c583014320a568592f5d1f5685de40d7c64f5e5fe8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45373dae92aa5007d34f749e78b0e5899e1a7c3c1ce4329315c3a5d7969c469b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cffa7afe37dfd330f9aa05e82a6f05a309d0d2079e615fcab933f7b9ead0d7`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 19.4 MB (19419747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f4ab1b20e761366e4592a4a695a67d6fb6ad55c780094fad9976df3ebeb21`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477c725c69905fa95c18552eb154560a212870c86cb468c7570ef9beea16e8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade21b9c6cec037cb7d2f205612a41a75789f0857a3304753e001984561e9983`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7311ebb09d47c704ac9a5d171113840b634120dc0c680eb276a91ddee2efd`  
		Last Modified: Tue, 11 Nov 2025 01:44:35 GMT  
		Size: 23.2 MB (23163257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28603a23c96e1bd9ba9ee0b8e4c446e6e01e8f268c3b8a292c4b7749184649d5`  
		Last Modified: Tue, 11 Nov 2025 01:44:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e94373564db23e5d8ea9cc012d861df363325d542c9908aee4273fe0a84566`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c07acbdd0f1cc9183784756376bc05490f3e9257490fc0a387eceb8ff38c645`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be490461e18aba4834222d552c012a6093108c1e590650b34829a457e978bc8c`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 22.7 MB (22677281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9c96d3736d1657483916877049c0ccbdb057a8df315fcb3e663048acfbd132d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:4da74ebb24ba1ed05d837769e2868b3fced76e9d625b5033e5c6bd554dba5b1c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1642975859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b248f8970d471ca71d2fe5d8cf5a618741a9ae195807e67894fa707304be22f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Tue, 11 Nov 2025 01:31:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:32:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:32:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:32:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:33:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:08 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:33:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:33:10 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:33:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:33:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:33:32 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:33:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607358d94499b322187d8294abffa374df336a542ba3a7746e54550a559a84e3`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff233fc8be81f08e0fd27b16161e9cb9e883edbeeb55293e4f90cf045577ee6b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 510.8 KB (510798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5647cb091467ce953f8492c583014320a568592f5d1f5685de40d7c64f5e5fe8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45373dae92aa5007d34f749e78b0e5899e1a7c3c1ce4329315c3a5d7969c469b`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cffa7afe37dfd330f9aa05e82a6f05a309d0d2079e615fcab933f7b9ead0d7`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 19.4 MB (19419747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f4ab1b20e761366e4592a4a695a67d6fb6ad55c780094fad9976df3ebeb21`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477c725c69905fa95c18552eb154560a212870c86cb468c7570ef9beea16e8`  
		Last Modified: Tue, 11 Nov 2025 01:44:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade21b9c6cec037cb7d2f205612a41a75789f0857a3304753e001984561e9983`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7311ebb09d47c704ac9a5d171113840b634120dc0c680eb276a91ddee2efd`  
		Last Modified: Tue, 11 Nov 2025 01:44:35 GMT  
		Size: 23.2 MB (23163257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28603a23c96e1bd9ba9ee0b8e4c446e6e01e8f268c3b8a292c4b7749184649d5`  
		Last Modified: Tue, 11 Nov 2025 01:44:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e94373564db23e5d8ea9cc012d861df363325d542c9908aee4273fe0a84566`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c07acbdd0f1cc9183784756376bc05490f3e9257490fc0a387eceb8ff38c645`  
		Last Modified: Tue, 11 Nov 2025 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be490461e18aba4834222d552c012a6093108c1e590650b34829a457e978bc8c`  
		Last Modified: Tue, 11 Nov 2025 01:44:32 GMT  
		Size: 22.7 MB (22677281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:cf52fc75c50a0b3ee0fd34f484cb9e7aa12c6b6f6187e520f1fc9cb2a96807fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:d3430dae25034c55c56dd585271ca3ff7633e012a1ba11f1498b04f25693ef2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3286034630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d734e887c89ba0c951f704dfa1208365d6a2457d51ed341c05d8223c37bd652a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Tue, 11 Nov 2025 01:09:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:09:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:09:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:09:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:09:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:09:59 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:10:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:10:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:10:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cbb13e31831b4a401483474d0b3761d526123e4940ffefb9e59ca0b95bd928`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11778e4fa17626dc91d9d9cb467403166f0cc6134bcadc2c6c394c23f4f77350`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 385.3 KB (385346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea88d46cd119b0ed069843b33c117aa143e9f6c36695cf17ee648d8dcf3655b`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa5fa37b5931fe92505e086ba67d6dfb0da4ae0172b58b04d5bb013277f60b9`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ada5899e6769690fd204f9f137706c9612fa97a65835249036bb92593e5eb`  
		Last Modified: Tue, 11 Nov 2025 01:19:20 GMT  
		Size: 19.4 MB (19430246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0272441663d6fec957c0b4d34b58b8a19b8808f1771c45d4c591dff46cb951`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918e1ab8b826581917ab7b2d53b2c6a5f2b06ce5c03f208c14dea008b3cfe60`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce36d1376a231ae8f91e59637fe876b6fa19bccb1bfd0a4e96c4d2b5d24a5ae5`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f749f808cf8c30f6a915e56d9393b185ef4a06c9ab0ce38fab25952828f43c6d`  
		Last Modified: Tue, 11 Nov 2025 01:19:18 GMT  
		Size: 23.2 MB (23173614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4c6efb8d391dc41567c8e29c5f2c1aaa0d6372c5dab092454b25133fbaf22`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f789efcc4cd75dab1e0486cceffa4fbb47564e174bfb011d328003e81c690ad`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73f4b7bd98ba3e36992613125ce4ea0186486089e65bd5b3be8e14604b916f0`  
		Last Modified: Tue, 11 Nov 2025 01:19:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ae4ce13bc5f392ee40f76f48ccf05ef5a576bd04b4b7affecfadde7443a36`  
		Last Modified: Tue, 11 Nov 2025 01:19:22 GMT  
		Size: 22.7 MB (22686606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
