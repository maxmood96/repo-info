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
-	[`docker:29.0.1`](#docker2901)
-	[`docker:29.0.1-alpine3.22`](#docker2901-alpine322)
-	[`docker:29.0.1-cli`](#docker2901-cli)
-	[`docker:29.0.1-cli-alpine3.22`](#docker2901-cli-alpine322)
-	[`docker:29.0.1-dind`](#docker2901-dind)
-	[`docker:29.0.1-dind-alpine3.22`](#docker2901-dind-alpine322)
-	[`docker:29.0.1-dind-rootless`](#docker2901-dind-rootless)
-	[`docker:29.0.1-windowsservercore`](#docker2901-windowsservercore)
-	[`docker:29.0.1-windowsservercore-ltsc2022`](#docker2901-windowsservercore-ltsc2022)
-	[`docker:29.0.1-windowsservercore-ltsc2025`](#docker2901-windowsservercore-ltsc2025)
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
$ docker pull docker@sha256:f7d048590d889e00868920f658e807ecbc4ef662d51c9af67eb5534a447d58d6
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
$ docker pull docker@sha256:b7941b2ccd806a2c6a86a9358773aa88b14b7917ed8a22af6147b1eac167ea37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75444849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5610201729349c6a70dcb8338e5ec33e1443f2a4b390f2ace27c542e2a6551f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6639e11997628dd93c3b8971e3df09ddec13aa1090dc25e18cfd82700144c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c10f48a4154ccf09427898d95780e35a51b74f0b0868fdf8bf3914dd5e150a7`

```dockerfile
```

-	Layers:
	-	`sha256:5acd60ebabd269e3bf29e690ffb732d33fc40c5b1d23c927a1bd86937a022403`  
		Last Modified: Fri, 14 Nov 2025 18:07:45 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:de3b12999906ced6af004389ff60e8d522230851392fd1d98c2f4b1d3a3d7aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71155509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6227483b507c988892ab228db7529b849e20aaf937ee76232ab743e0ce2382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9a87490926570243a4d251dae8b8f569662ae5af2de5025d53a42d0d08d0b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7ce2655c6bf1df9638a7a64d777afe8ed589e15bc4098a644382eeed483709`

```dockerfile
```

-	Layers:
	-	`sha256:3ff99371b5cd8e73694b7d6b254cf527f48f5f727a79d676088cccb0830d0c89`  
		Last Modified: Fri, 14 Nov 2025 18:07:48 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:76c19db0b5751c3df03c26f0ce3ce68ab059831cb81e504f8134059758b7f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4abaf932f47f68cd8df61080df26ae2934afa32af1ef9b0199884a9b3f6ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0890e3f571d08c5d82e6a43cf4c59460170ceb9b1ff8421ea78ff9e5276788f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5368d0b81e1020cfbb376075883e1424d7ea529a38d09e4c5f6180d1ea0ee`

```dockerfile
```

-	Layers:
	-	`sha256:462519a6a1755237bf46e1f96ab675d3615d2ed4d23deac96faf17e878615c8c`  
		Last Modified: Fri, 14 Nov 2025 18:07:52 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9009a0bbad1078191e0b701bba772bfaf33f06c4aeabd0c88847cd12e27bb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70238617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47e3268b71de1f8d2b3f16253789c894ccb5c517327e000fe4f04b56b4a700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6c4b38a379125c5a42c9424120314522bbc3c2207ec499983e38878b7fdab640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a750656c16998bce5538dc78fb7d4ee4a8651174daaa388d58a43742ed6c3b`

```dockerfile
```

-	Layers:
	-	`sha256:bd54fcfe11ce172467cf267a5b45ac604e052195b987a6ae1c5642e94d12397e`  
		Last Modified: Fri, 14 Nov 2025 18:07:55 GMT  
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
$ docker pull docker@sha256:74a523ff73f42a4d448126abcb68c8eeeb59a6612c97ace71ebea173950e80d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:f837bce39539584466c46e594b9f0c81b35795836721c08982a0f91d997200ea
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301029232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fde49f87e1cd7da85aad033b1d1565aebb9dbefd76b70cd81c19b094a439b94`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:11:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:56 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77d76091b7aac8a391dc15a412eec8b3ee40fe1bc86700413bb69bf1114e676`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57705bc4aa1e453e214669340c20ec44256db4da801f3106104ec20b93a80c6f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 339.3 KB (339255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e61534cc65875c590fe7e13a58c5f1c9f383d3df204ef1521b2c0e5978b459`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569dbb4820f686d3922f9c91d52b813af356bd690ae149348371d6e4caca4a5f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096d3c32f2105107d2ec689004dccd74709d115af77d5eafda417975a32ec423`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 19.4 MB (19407554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f5caf299e5f728ab68863aa2a83d98bab228edde6131d35105563a6d6e5402`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac53906e4375308fd4355425554c6e38107ad3d406848d4de359fba65c86b2`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a69edd0f0500bed085e20dec378ea3173a1ea772a5f0f13b29c2ce48881e7b0`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cbe51dd737e36d3aede4692a695eccfecb33dd785265e7db9b103940127341`  
		Last Modified: Tue, 11 Nov 2025 19:22:21 GMT  
		Size: 23.2 MB (23150833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a45652de8491119468d0f7b6191c70a97ab841b0f1aaf118d7979de6132670e`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e7c49ef5aecb14f6ff4eb109d9465851171bc3328322ab7e18302b62e1a593`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daee60478741bde59ff4678f7189b7e2b89236f4df16b5c63ead8be0b3db8023`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e7271db460caf1303e74ff32ba6f1d3f45b3626177d4c5b119ccbfa96cf584`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 22.7 MB (22663991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:547723ea04909125526cb23fb563a46f2301df0a926f022573f2b0621df0b552
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835714555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6225acdf513d523a4e5f171654574cf1b2f06e39f7423c786533420be8ad7ae8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:35 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:52 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77379ef0e0e6736861441fc459538ec29a38e2695e5072007d019bd55c2fa950`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 497.9 KB (497949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899bdb2c9a06e8c2bd2121c8f6f9737c19f54e7f844bbf73604a3f955247d131`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a997f06dcced75ecdce2c08dc44619e9b9de11091760c69018ec1de6dadc8315`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b071036fe41b378649b062f3a9d6a8501a432a05718e96d042145b4d0d31af4`  
		Last Modified: Tue, 11 Nov 2025 19:18:53 GMT  
		Size: 19.4 MB (19414195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a96e400b09393f86048b9d3b56db0ae7eacb0b20e85eccd2496fe5d26d99a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5198f20bbc902ae2b9e919aa8f67bfb4994f46f9412d09affd43bdb5de4295e1`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e011cb046f9715e7264a714fff85c39cba7caf6d835e6da94de151a415a8d77`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9defe4698fab9ed347e44988419378e6b6bc431be8c5f520706fb34a4099e779`  
		Last Modified: Tue, 11 Nov 2025 19:18:55 GMT  
		Size: 23.2 MB (23158195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaca05470ddd0a069854418864ae4c00f6bd02495ea14fbae2adeee5662a30a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285f45b248227884bd5620c2513c0d53a44d08a7a074b2eaa6b45912824505e3`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d3b5c97ff7ce75236dee3b1b8cbdf540f062fb5eff8cfbc214609a9afd6e0`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8886e8fb24b2ac72d10b24a72eaddcb7d21a66772414a2196be5e92e1d0107f1`  
		Last Modified: Tue, 11 Nov 2025 19:18:54 GMT  
		Size: 22.7 MB (22670905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:640fb0eed94a4f803f7e799f959e7c8a1ca342a0c0c219abf7d7995586e241c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:547723ea04909125526cb23fb563a46f2301df0a926f022573f2b0621df0b552
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835714555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6225acdf513d523a4e5f171654574cf1b2f06e39f7423c786533420be8ad7ae8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:35 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:52 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77379ef0e0e6736861441fc459538ec29a38e2695e5072007d019bd55c2fa950`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 497.9 KB (497949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899bdb2c9a06e8c2bd2121c8f6f9737c19f54e7f844bbf73604a3f955247d131`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a997f06dcced75ecdce2c08dc44619e9b9de11091760c69018ec1de6dadc8315`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b071036fe41b378649b062f3a9d6a8501a432a05718e96d042145b4d0d31af4`  
		Last Modified: Tue, 11 Nov 2025 19:18:53 GMT  
		Size: 19.4 MB (19414195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a96e400b09393f86048b9d3b56db0ae7eacb0b20e85eccd2496fe5d26d99a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5198f20bbc902ae2b9e919aa8f67bfb4994f46f9412d09affd43bdb5de4295e1`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e011cb046f9715e7264a714fff85c39cba7caf6d835e6da94de151a415a8d77`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9defe4698fab9ed347e44988419378e6b6bc431be8c5f520706fb34a4099e779`  
		Last Modified: Tue, 11 Nov 2025 19:18:55 GMT  
		Size: 23.2 MB (23158195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaca05470ddd0a069854418864ae4c00f6bd02495ea14fbae2adeee5662a30a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285f45b248227884bd5620c2513c0d53a44d08a7a074b2eaa6b45912824505e3`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d3b5c97ff7ce75236dee3b1b8cbdf540f062fb5eff8cfbc214609a9afd6e0`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8886e8fb24b2ac72d10b24a72eaddcb7d21a66772414a2196be5e92e1d0107f1`  
		Last Modified: Tue, 11 Nov 2025 19:18:54 GMT  
		Size: 22.7 MB (22670905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:529e79f77f256c18d3449ee2b3afe778b7ac252226391cfcf83a54e16b1f83c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:f837bce39539584466c46e594b9f0c81b35795836721c08982a0f91d997200ea
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301029232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fde49f87e1cd7da85aad033b1d1565aebb9dbefd76b70cd81c19b094a439b94`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:11:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:56 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77d76091b7aac8a391dc15a412eec8b3ee40fe1bc86700413bb69bf1114e676`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57705bc4aa1e453e214669340c20ec44256db4da801f3106104ec20b93a80c6f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 339.3 KB (339255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e61534cc65875c590fe7e13a58c5f1c9f383d3df204ef1521b2c0e5978b459`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569dbb4820f686d3922f9c91d52b813af356bd690ae149348371d6e4caca4a5f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096d3c32f2105107d2ec689004dccd74709d115af77d5eafda417975a32ec423`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 19.4 MB (19407554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f5caf299e5f728ab68863aa2a83d98bab228edde6131d35105563a6d6e5402`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac53906e4375308fd4355425554c6e38107ad3d406848d4de359fba65c86b2`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a69edd0f0500bed085e20dec378ea3173a1ea772a5f0f13b29c2ce48881e7b0`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cbe51dd737e36d3aede4692a695eccfecb33dd785265e7db9b103940127341`  
		Last Modified: Tue, 11 Nov 2025 19:22:21 GMT  
		Size: 23.2 MB (23150833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a45652de8491119468d0f7b6191c70a97ab841b0f1aaf118d7979de6132670e`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e7c49ef5aecb14f6ff4eb109d9465851171bc3328322ab7e18302b62e1a593`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daee60478741bde59ff4678f7189b7e2b89236f4df16b5c63ead8be0b3db8023`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e7271db460caf1303e74ff32ba6f1d3f45b3626177d4c5b119ccbfa96cf584`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 22.7 MB (22663991 bytes)  
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
$ docker pull docker@sha256:f7d048590d889e00868920f658e807ecbc4ef662d51c9af67eb5534a447d58d6
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
$ docker pull docker@sha256:b7941b2ccd806a2c6a86a9358773aa88b14b7917ed8a22af6147b1eac167ea37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75444849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5610201729349c6a70dcb8338e5ec33e1443f2a4b390f2ace27c542e2a6551f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6639e11997628dd93c3b8971e3df09ddec13aa1090dc25e18cfd82700144c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c10f48a4154ccf09427898d95780e35a51b74f0b0868fdf8bf3914dd5e150a7`

```dockerfile
```

-	Layers:
	-	`sha256:5acd60ebabd269e3bf29e690ffb732d33fc40c5b1d23c927a1bd86937a022403`  
		Last Modified: Fri, 14 Nov 2025 18:07:45 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:de3b12999906ced6af004389ff60e8d522230851392fd1d98c2f4b1d3a3d7aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71155509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6227483b507c988892ab228db7529b849e20aaf937ee76232ab743e0ce2382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9a87490926570243a4d251dae8b8f569662ae5af2de5025d53a42d0d08d0b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7ce2655c6bf1df9638a7a64d777afe8ed589e15bc4098a644382eeed483709`

```dockerfile
```

-	Layers:
	-	`sha256:3ff99371b5cd8e73694b7d6b254cf527f48f5f727a79d676088cccb0830d0c89`  
		Last Modified: Fri, 14 Nov 2025 18:07:48 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:76c19db0b5751c3df03c26f0ce3ce68ab059831cb81e504f8134059758b7f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4abaf932f47f68cd8df61080df26ae2934afa32af1ef9b0199884a9b3f6ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0890e3f571d08c5d82e6a43cf4c59460170ceb9b1ff8421ea78ff9e5276788f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5368d0b81e1020cfbb376075883e1424d7ea529a38d09e4c5f6180d1ea0ee`

```dockerfile
```

-	Layers:
	-	`sha256:462519a6a1755237bf46e1f96ab675d3615d2ed4d23deac96faf17e878615c8c`  
		Last Modified: Fri, 14 Nov 2025 18:07:52 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9009a0bbad1078191e0b701bba772bfaf33f06c4aeabd0c88847cd12e27bb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70238617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47e3268b71de1f8d2b3f16253789c894ccb5c517327e000fe4f04b56b4a700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6c4b38a379125c5a42c9424120314522bbc3c2207ec499983e38878b7fdab640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a750656c16998bce5538dc78fb7d4ee4a8651174daaa388d58a43742ed6c3b`

```dockerfile
```

-	Layers:
	-	`sha256:bd54fcfe11ce172467cf267a5b45ac604e052195b987a6ae1c5642e94d12397e`  
		Last Modified: Fri, 14 Nov 2025 18:07:55 GMT  
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
$ docker pull docker@sha256:74a523ff73f42a4d448126abcb68c8eeeb59a6612c97ace71ebea173950e80d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:29.0-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:f837bce39539584466c46e594b9f0c81b35795836721c08982a0f91d997200ea
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301029232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fde49f87e1cd7da85aad033b1d1565aebb9dbefd76b70cd81c19b094a439b94`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:11:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:56 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77d76091b7aac8a391dc15a412eec8b3ee40fe1bc86700413bb69bf1114e676`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57705bc4aa1e453e214669340c20ec44256db4da801f3106104ec20b93a80c6f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 339.3 KB (339255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e61534cc65875c590fe7e13a58c5f1c9f383d3df204ef1521b2c0e5978b459`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569dbb4820f686d3922f9c91d52b813af356bd690ae149348371d6e4caca4a5f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096d3c32f2105107d2ec689004dccd74709d115af77d5eafda417975a32ec423`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 19.4 MB (19407554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f5caf299e5f728ab68863aa2a83d98bab228edde6131d35105563a6d6e5402`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac53906e4375308fd4355425554c6e38107ad3d406848d4de359fba65c86b2`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a69edd0f0500bed085e20dec378ea3173a1ea772a5f0f13b29c2ce48881e7b0`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cbe51dd737e36d3aede4692a695eccfecb33dd785265e7db9b103940127341`  
		Last Modified: Tue, 11 Nov 2025 19:22:21 GMT  
		Size: 23.2 MB (23150833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a45652de8491119468d0f7b6191c70a97ab841b0f1aaf118d7979de6132670e`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e7c49ef5aecb14f6ff4eb109d9465851171bc3328322ab7e18302b62e1a593`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daee60478741bde59ff4678f7189b7e2b89236f4df16b5c63ead8be0b3db8023`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e7271db460caf1303e74ff32ba6f1d3f45b3626177d4c5b119ccbfa96cf584`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 22.7 MB (22663991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.0-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:547723ea04909125526cb23fb563a46f2301df0a926f022573f2b0621df0b552
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835714555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6225acdf513d523a4e5f171654574cf1b2f06e39f7423c786533420be8ad7ae8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:35 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:52 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77379ef0e0e6736861441fc459538ec29a38e2695e5072007d019bd55c2fa950`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 497.9 KB (497949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899bdb2c9a06e8c2bd2121c8f6f9737c19f54e7f844bbf73604a3f955247d131`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a997f06dcced75ecdce2c08dc44619e9b9de11091760c69018ec1de6dadc8315`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b071036fe41b378649b062f3a9d6a8501a432a05718e96d042145b4d0d31af4`  
		Last Modified: Tue, 11 Nov 2025 19:18:53 GMT  
		Size: 19.4 MB (19414195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a96e400b09393f86048b9d3b56db0ae7eacb0b20e85eccd2496fe5d26d99a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5198f20bbc902ae2b9e919aa8f67bfb4994f46f9412d09affd43bdb5de4295e1`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e011cb046f9715e7264a714fff85c39cba7caf6d835e6da94de151a415a8d77`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9defe4698fab9ed347e44988419378e6b6bc431be8c5f520706fb34a4099e779`  
		Last Modified: Tue, 11 Nov 2025 19:18:55 GMT  
		Size: 23.2 MB (23158195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaca05470ddd0a069854418864ae4c00f6bd02495ea14fbae2adeee5662a30a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285f45b248227884bd5620c2513c0d53a44d08a7a074b2eaa6b45912824505e3`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d3b5c97ff7ce75236dee3b1b8cbdf540f062fb5eff8cfbc214609a9afd6e0`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8886e8fb24b2ac72d10b24a72eaddcb7d21a66772414a2196be5e92e1d0107f1`  
		Last Modified: Tue, 11 Nov 2025 19:18:54 GMT  
		Size: 22.7 MB (22670905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:640fb0eed94a4f803f7e799f959e7c8a1ca342a0c0c219abf7d7995586e241c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:29.0-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:547723ea04909125526cb23fb563a46f2301df0a926f022573f2b0621df0b552
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835714555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6225acdf513d523a4e5f171654574cf1b2f06e39f7423c786533420be8ad7ae8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:35 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:52 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77379ef0e0e6736861441fc459538ec29a38e2695e5072007d019bd55c2fa950`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 497.9 KB (497949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899bdb2c9a06e8c2bd2121c8f6f9737c19f54e7f844bbf73604a3f955247d131`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a997f06dcced75ecdce2c08dc44619e9b9de11091760c69018ec1de6dadc8315`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b071036fe41b378649b062f3a9d6a8501a432a05718e96d042145b4d0d31af4`  
		Last Modified: Tue, 11 Nov 2025 19:18:53 GMT  
		Size: 19.4 MB (19414195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a96e400b09393f86048b9d3b56db0ae7eacb0b20e85eccd2496fe5d26d99a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5198f20bbc902ae2b9e919aa8f67bfb4994f46f9412d09affd43bdb5de4295e1`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e011cb046f9715e7264a714fff85c39cba7caf6d835e6da94de151a415a8d77`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9defe4698fab9ed347e44988419378e6b6bc431be8c5f520706fb34a4099e779`  
		Last Modified: Tue, 11 Nov 2025 19:18:55 GMT  
		Size: 23.2 MB (23158195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaca05470ddd0a069854418864ae4c00f6bd02495ea14fbae2adeee5662a30a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285f45b248227884bd5620c2513c0d53a44d08a7a074b2eaa6b45912824505e3`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d3b5c97ff7ce75236dee3b1b8cbdf540f062fb5eff8cfbc214609a9afd6e0`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8886e8fb24b2ac72d10b24a72eaddcb7d21a66772414a2196be5e92e1d0107f1`  
		Last Modified: Tue, 11 Nov 2025 19:18:54 GMT  
		Size: 22.7 MB (22670905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:529e79f77f256c18d3449ee2b3afe778b7ac252226391cfcf83a54e16b1f83c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:29.0-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:f837bce39539584466c46e594b9f0c81b35795836721c08982a0f91d997200ea
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301029232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fde49f87e1cd7da85aad033b1d1565aebb9dbefd76b70cd81c19b094a439b94`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:11:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:56 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77d76091b7aac8a391dc15a412eec8b3ee40fe1bc86700413bb69bf1114e676`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57705bc4aa1e453e214669340c20ec44256db4da801f3106104ec20b93a80c6f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 339.3 KB (339255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e61534cc65875c590fe7e13a58c5f1c9f383d3df204ef1521b2c0e5978b459`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569dbb4820f686d3922f9c91d52b813af356bd690ae149348371d6e4caca4a5f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096d3c32f2105107d2ec689004dccd74709d115af77d5eafda417975a32ec423`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 19.4 MB (19407554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f5caf299e5f728ab68863aa2a83d98bab228edde6131d35105563a6d6e5402`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac53906e4375308fd4355425554c6e38107ad3d406848d4de359fba65c86b2`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a69edd0f0500bed085e20dec378ea3173a1ea772a5f0f13b29c2ce48881e7b0`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cbe51dd737e36d3aede4692a695eccfecb33dd785265e7db9b103940127341`  
		Last Modified: Tue, 11 Nov 2025 19:22:21 GMT  
		Size: 23.2 MB (23150833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a45652de8491119468d0f7b6191c70a97ab841b0f1aaf118d7979de6132670e`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e7c49ef5aecb14f6ff4eb109d9465851171bc3328322ab7e18302b62e1a593`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daee60478741bde59ff4678f7189b7e2b89236f4df16b5c63ead8be0b3db8023`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e7271db460caf1303e74ff32ba6f1d3f45b3626177d4c5b119ccbfa96cf584`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 22.7 MB (22663991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0.1`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.0.1-alpine3.22`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.0.1-cli`

```console
$ docker pull docker@sha256:f7d048590d889e00868920f658e807ecbc4ef662d51c9af67eb5534a447d58d6
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

### `docker:29.0.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:b7941b2ccd806a2c6a86a9358773aa88b14b7917ed8a22af6147b1eac167ea37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75444849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5610201729349c6a70dcb8338e5ec33e1443f2a4b390f2ace27c542e2a6551f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6639e11997628dd93c3b8971e3df09ddec13aa1090dc25e18cfd82700144c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c10f48a4154ccf09427898d95780e35a51b74f0b0868fdf8bf3914dd5e150a7`

```dockerfile
```

-	Layers:
	-	`sha256:5acd60ebabd269e3bf29e690ffb732d33fc40c5b1d23c927a1bd86937a022403`  
		Last Modified: Fri, 14 Nov 2025 18:07:45 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:de3b12999906ced6af004389ff60e8d522230851392fd1d98c2f4b1d3a3d7aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71155509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6227483b507c988892ab228db7529b849e20aaf937ee76232ab743e0ce2382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9a87490926570243a4d251dae8b8f569662ae5af2de5025d53a42d0d08d0b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7ce2655c6bf1df9638a7a64d777afe8ed589e15bc4098a644382eeed483709`

```dockerfile
```

-	Layers:
	-	`sha256:3ff99371b5cd8e73694b7d6b254cf527f48f5f727a79d676088cccb0830d0c89`  
		Last Modified: Fri, 14 Nov 2025 18:07:48 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:76c19db0b5751c3df03c26f0ce3ce68ab059831cb81e504f8134059758b7f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4abaf932f47f68cd8df61080df26ae2934afa32af1ef9b0199884a9b3f6ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0890e3f571d08c5d82e6a43cf4c59460170ceb9b1ff8421ea78ff9e5276788f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5368d0b81e1020cfbb376075883e1424d7ea529a38d09e4c5f6180d1ea0ee`

```dockerfile
```

-	Layers:
	-	`sha256:462519a6a1755237bf46e1f96ab675d3615d2ed4d23deac96faf17e878615c8c`  
		Last Modified: Fri, 14 Nov 2025 18:07:52 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9009a0bbad1078191e0b701bba772bfaf33f06c4aeabd0c88847cd12e27bb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70238617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47e3268b71de1f8d2b3f16253789c894ccb5c517327e000fe4f04b56b4a700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6c4b38a379125c5a42c9424120314522bbc3c2207ec499983e38878b7fdab640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a750656c16998bce5538dc78fb7d4ee4a8651174daaa388d58a43742ed6c3b`

```dockerfile
```

-	Layers:
	-	`sha256:bd54fcfe11ce172467cf267a5b45ac604e052195b987a6ae1c5642e94d12397e`  
		Last Modified: Fri, 14 Nov 2025 18:07:55 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.1-cli-alpine3.22`

```console
$ docker pull docker@sha256:f7d048590d889e00868920f658e807ecbc4ef662d51c9af67eb5534a447d58d6
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

### `docker:29.0.1-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:b7941b2ccd806a2c6a86a9358773aa88b14b7917ed8a22af6147b1eac167ea37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75444849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5610201729349c6a70dcb8338e5ec33e1443f2a4b390f2ace27c542e2a6551f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6639e11997628dd93c3b8971e3df09ddec13aa1090dc25e18cfd82700144c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c10f48a4154ccf09427898d95780e35a51b74f0b0868fdf8bf3914dd5e150a7`

```dockerfile
```

-	Layers:
	-	`sha256:5acd60ebabd269e3bf29e690ffb732d33fc40c5b1d23c927a1bd86937a022403`  
		Last Modified: Fri, 14 Nov 2025 18:07:45 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:de3b12999906ced6af004389ff60e8d522230851392fd1d98c2f4b1d3a3d7aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71155509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6227483b507c988892ab228db7529b849e20aaf937ee76232ab743e0ce2382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:9a87490926570243a4d251dae8b8f569662ae5af2de5025d53a42d0d08d0b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7ce2655c6bf1df9638a7a64d777afe8ed589e15bc4098a644382eeed483709`

```dockerfile
```

-	Layers:
	-	`sha256:3ff99371b5cd8e73694b7d6b254cf527f48f5f727a79d676088cccb0830d0c89`  
		Last Modified: Fri, 14 Nov 2025 18:07:48 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:76c19db0b5751c3df03c26f0ce3ce68ab059831cb81e504f8134059758b7f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4abaf932f47f68cd8df61080df26ae2934afa32af1ef9b0199884a9b3f6ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:0890e3f571d08c5d82e6a43cf4c59460170ceb9b1ff8421ea78ff9e5276788f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5368d0b81e1020cfbb376075883e1424d7ea529a38d09e4c5f6180d1ea0ee`

```dockerfile
```

-	Layers:
	-	`sha256:462519a6a1755237bf46e1f96ab675d3615d2ed4d23deac96faf17e878615c8c`  
		Last Modified: Fri, 14 Nov 2025 18:07:52 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9009a0bbad1078191e0b701bba772bfaf33f06c4aeabd0c88847cd12e27bb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70238617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47e3268b71de1f8d2b3f16253789c894ccb5c517327e000fe4f04b56b4a700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6c4b38a379125c5a42c9424120314522bbc3c2207ec499983e38878b7fdab640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a750656c16998bce5538dc78fb7d4ee4a8651174daaa388d58a43742ed6c3b`

```dockerfile
```

-	Layers:
	-	`sha256:bd54fcfe11ce172467cf267a5b45ac604e052195b987a6ae1c5642e94d12397e`  
		Last Modified: Fri, 14 Nov 2025 18:07:55 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.1-dind`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.0.1-dind-alpine3.22`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.0.1-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.0.1-windowsservercore`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.0.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.0.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:cli`

```console
$ docker pull docker@sha256:f7d048590d889e00868920f658e807ecbc4ef662d51c9af67eb5534a447d58d6
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
$ docker pull docker@sha256:b7941b2ccd806a2c6a86a9358773aa88b14b7917ed8a22af6147b1eac167ea37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75444849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5610201729349c6a70dcb8338e5ec33e1443f2a4b390f2ace27c542e2a6551f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6639e11997628dd93c3b8971e3df09ddec13aa1090dc25e18cfd82700144c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c10f48a4154ccf09427898d95780e35a51b74f0b0868fdf8bf3914dd5e150a7`

```dockerfile
```

-	Layers:
	-	`sha256:5acd60ebabd269e3bf29e690ffb732d33fc40c5b1d23c927a1bd86937a022403`  
		Last Modified: Fri, 14 Nov 2025 18:07:45 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:de3b12999906ced6af004389ff60e8d522230851392fd1d98c2f4b1d3a3d7aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71155509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6227483b507c988892ab228db7529b849e20aaf937ee76232ab743e0ce2382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:9a87490926570243a4d251dae8b8f569662ae5af2de5025d53a42d0d08d0b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7ce2655c6bf1df9638a7a64d777afe8ed589e15bc4098a644382eeed483709`

```dockerfile
```

-	Layers:
	-	`sha256:3ff99371b5cd8e73694b7d6b254cf527f48f5f727a79d676088cccb0830d0c89`  
		Last Modified: Fri, 14 Nov 2025 18:07:48 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:76c19db0b5751c3df03c26f0ce3ce68ab059831cb81e504f8134059758b7f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4abaf932f47f68cd8df61080df26ae2934afa32af1ef9b0199884a9b3f6ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0890e3f571d08c5d82e6a43cf4c59460170ceb9b1ff8421ea78ff9e5276788f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5368d0b81e1020cfbb376075883e1424d7ea529a38d09e4c5f6180d1ea0ee`

```dockerfile
```

-	Layers:
	-	`sha256:462519a6a1755237bf46e1f96ab675d3615d2ed4d23deac96faf17e878615c8c`  
		Last Modified: Fri, 14 Nov 2025 18:07:52 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9009a0bbad1078191e0b701bba772bfaf33f06c4aeabd0c88847cd12e27bb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70238617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47e3268b71de1f8d2b3f16253789c894ccb5c517327e000fe4f04b56b4a700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6c4b38a379125c5a42c9424120314522bbc3c2207ec499983e38878b7fdab640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a750656c16998bce5538dc78fb7d4ee4a8651174daaa388d58a43742ed6c3b`

```dockerfile
```

-	Layers:
	-	`sha256:bd54fcfe11ce172467cf267a5b45ac604e052195b987a6ae1c5642e94d12397e`  
		Last Modified: Fri, 14 Nov 2025 18:07:55 GMT  
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
$ docker pull docker@sha256:74a523ff73f42a4d448126abcb68c8eeeb59a6612c97ace71ebea173950e80d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:f837bce39539584466c46e594b9f0c81b35795836721c08982a0f91d997200ea
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301029232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fde49f87e1cd7da85aad033b1d1565aebb9dbefd76b70cd81c19b094a439b94`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:11:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:56 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77d76091b7aac8a391dc15a412eec8b3ee40fe1bc86700413bb69bf1114e676`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57705bc4aa1e453e214669340c20ec44256db4da801f3106104ec20b93a80c6f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 339.3 KB (339255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e61534cc65875c590fe7e13a58c5f1c9f383d3df204ef1521b2c0e5978b459`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569dbb4820f686d3922f9c91d52b813af356bd690ae149348371d6e4caca4a5f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096d3c32f2105107d2ec689004dccd74709d115af77d5eafda417975a32ec423`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 19.4 MB (19407554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f5caf299e5f728ab68863aa2a83d98bab228edde6131d35105563a6d6e5402`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac53906e4375308fd4355425554c6e38107ad3d406848d4de359fba65c86b2`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a69edd0f0500bed085e20dec378ea3173a1ea772a5f0f13b29c2ce48881e7b0`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cbe51dd737e36d3aede4692a695eccfecb33dd785265e7db9b103940127341`  
		Last Modified: Tue, 11 Nov 2025 19:22:21 GMT  
		Size: 23.2 MB (23150833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a45652de8491119468d0f7b6191c70a97ab841b0f1aaf118d7979de6132670e`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e7c49ef5aecb14f6ff4eb109d9465851171bc3328322ab7e18302b62e1a593`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daee60478741bde59ff4678f7189b7e2b89236f4df16b5c63ead8be0b3db8023`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e7271db460caf1303e74ff32ba6f1d3f45b3626177d4c5b119ccbfa96cf584`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 22.7 MB (22663991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:547723ea04909125526cb23fb563a46f2301df0a926f022573f2b0621df0b552
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835714555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6225acdf513d523a4e5f171654574cf1b2f06e39f7423c786533420be8ad7ae8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:35 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:52 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77379ef0e0e6736861441fc459538ec29a38e2695e5072007d019bd55c2fa950`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 497.9 KB (497949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899bdb2c9a06e8c2bd2121c8f6f9737c19f54e7f844bbf73604a3f955247d131`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a997f06dcced75ecdce2c08dc44619e9b9de11091760c69018ec1de6dadc8315`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b071036fe41b378649b062f3a9d6a8501a432a05718e96d042145b4d0d31af4`  
		Last Modified: Tue, 11 Nov 2025 19:18:53 GMT  
		Size: 19.4 MB (19414195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a96e400b09393f86048b9d3b56db0ae7eacb0b20e85eccd2496fe5d26d99a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5198f20bbc902ae2b9e919aa8f67bfb4994f46f9412d09affd43bdb5de4295e1`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e011cb046f9715e7264a714fff85c39cba7caf6d835e6da94de151a415a8d77`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9defe4698fab9ed347e44988419378e6b6bc431be8c5f520706fb34a4099e779`  
		Last Modified: Tue, 11 Nov 2025 19:18:55 GMT  
		Size: 23.2 MB (23158195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaca05470ddd0a069854418864ae4c00f6bd02495ea14fbae2adeee5662a30a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285f45b248227884bd5620c2513c0d53a44d08a7a074b2eaa6b45912824505e3`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d3b5c97ff7ce75236dee3b1b8cbdf540f062fb5eff8cfbc214609a9afd6e0`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8886e8fb24b2ac72d10b24a72eaddcb7d21a66772414a2196be5e92e1d0107f1`  
		Last Modified: Tue, 11 Nov 2025 19:18:54 GMT  
		Size: 22.7 MB (22670905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:640fb0eed94a4f803f7e799f959e7c8a1ca342a0c0c219abf7d7995586e241c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:547723ea04909125526cb23fb563a46f2301df0a926f022573f2b0621df0b552
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835714555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6225acdf513d523a4e5f171654574cf1b2f06e39f7423c786533420be8ad7ae8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:35 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:52 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77379ef0e0e6736861441fc459538ec29a38e2695e5072007d019bd55c2fa950`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 497.9 KB (497949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899bdb2c9a06e8c2bd2121c8f6f9737c19f54e7f844bbf73604a3f955247d131`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a997f06dcced75ecdce2c08dc44619e9b9de11091760c69018ec1de6dadc8315`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b071036fe41b378649b062f3a9d6a8501a432a05718e96d042145b4d0d31af4`  
		Last Modified: Tue, 11 Nov 2025 19:18:53 GMT  
		Size: 19.4 MB (19414195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a96e400b09393f86048b9d3b56db0ae7eacb0b20e85eccd2496fe5d26d99a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5198f20bbc902ae2b9e919aa8f67bfb4994f46f9412d09affd43bdb5de4295e1`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e011cb046f9715e7264a714fff85c39cba7caf6d835e6da94de151a415a8d77`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9defe4698fab9ed347e44988419378e6b6bc431be8c5f520706fb34a4099e779`  
		Last Modified: Tue, 11 Nov 2025 19:18:55 GMT  
		Size: 23.2 MB (23158195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaca05470ddd0a069854418864ae4c00f6bd02495ea14fbae2adeee5662a30a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285f45b248227884bd5620c2513c0d53a44d08a7a074b2eaa6b45912824505e3`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d3b5c97ff7ce75236dee3b1b8cbdf540f062fb5eff8cfbc214609a9afd6e0`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8886e8fb24b2ac72d10b24a72eaddcb7d21a66772414a2196be5e92e1d0107f1`  
		Last Modified: Tue, 11 Nov 2025 19:18:54 GMT  
		Size: 22.7 MB (22670905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:529e79f77f256c18d3449ee2b3afe778b7ac252226391cfcf83a54e16b1f83c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:f837bce39539584466c46e594b9f0c81b35795836721c08982a0f91d997200ea
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301029232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fde49f87e1cd7da85aad033b1d1565aebb9dbefd76b70cd81c19b094a439b94`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:11:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:56 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77d76091b7aac8a391dc15a412eec8b3ee40fe1bc86700413bb69bf1114e676`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57705bc4aa1e453e214669340c20ec44256db4da801f3106104ec20b93a80c6f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 339.3 KB (339255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e61534cc65875c590fe7e13a58c5f1c9f383d3df204ef1521b2c0e5978b459`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569dbb4820f686d3922f9c91d52b813af356bd690ae149348371d6e4caca4a5f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096d3c32f2105107d2ec689004dccd74709d115af77d5eafda417975a32ec423`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 19.4 MB (19407554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f5caf299e5f728ab68863aa2a83d98bab228edde6131d35105563a6d6e5402`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac53906e4375308fd4355425554c6e38107ad3d406848d4de359fba65c86b2`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a69edd0f0500bed085e20dec378ea3173a1ea772a5f0f13b29c2ce48881e7b0`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cbe51dd737e36d3aede4692a695eccfecb33dd785265e7db9b103940127341`  
		Last Modified: Tue, 11 Nov 2025 19:22:21 GMT  
		Size: 23.2 MB (23150833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a45652de8491119468d0f7b6191c70a97ab841b0f1aaf118d7979de6132670e`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e7c49ef5aecb14f6ff4eb109d9465851171bc3328322ab7e18302b62e1a593`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daee60478741bde59ff4678f7189b7e2b89236f4df16b5c63ead8be0b3db8023`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e7271db460caf1303e74ff32ba6f1d3f45b3626177d4c5b119ccbfa96cf584`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 22.7 MB (22663991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
