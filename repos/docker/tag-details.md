<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.1`](#docker291)
-	[`docker:29.1-cli`](#docker291-cli)
-	[`docker:29.1-dind`](#docker291-dind)
-	[`docker:29.1-dind-rootless`](#docker291-dind-rootless)
-	[`docker:29.1-windowsservercore`](#docker291-windowsservercore)
-	[`docker:29.1-windowsservercore-ltsc2022`](#docker291-windowsservercore-ltsc2022)
-	[`docker:29.1-windowsservercore-ltsc2025`](#docker291-windowsservercore-ltsc2025)
-	[`docker:29.1.2`](#docker2912)
-	[`docker:29.1.2-alpine3.23`](#docker2912-alpine323)
-	[`docker:29.1.2-cli`](#docker2912-cli)
-	[`docker:29.1.2-cli-alpine3.23`](#docker2912-cli-alpine323)
-	[`docker:29.1.2-dind`](#docker2912-dind)
-	[`docker:29.1.2-dind-alpine3.23`](#docker2912-dind-alpine323)
-	[`docker:29.1.2-dind-rootless`](#docker2912-dind-rootless)
-	[`docker:29.1.2-windowsservercore`](#docker2912-windowsservercore)
-	[`docker:29.1.2-windowsservercore-ltsc2022`](#docker2912-windowsservercore-ltsc2022)
-	[`docker:29.1.2-windowsservercore-ltsc2025`](#docker2912-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:d47faf85fc5cb4283d7a20c95b6b02d012250b46ec26567554076e2767cb9093
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
$ docker pull docker@sha256:402b891668de1fe99eb7d054cf25df00a6217232585c02a509ecd7d89ee90856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135884343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b4440e17e983942d30f645a848d94efafacaef8be8733a99feeedc93b05165`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:730e45afac3924277c2d3d65bbd80e18019ece14ae5ca8ec59a55372c9357de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4237c7596712be121f7d034be83210391de8307b0ad7f32c6a82e65b63cd5899`

```dockerfile
```

-	Layers:
	-	`sha256:25e1d1a7097f30c7caefc7d07f5efc216727d9595749698f69ba2d3f3c9ac6ce`  
		Last Modified: Thu, 04 Dec 2025 03:07:31 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:fe601bbe28b63642b9b52b7a8478c09ad9007efb3307344dd0200e78ec89757d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128099244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11f21ae0c179baf1e0e49afea4c0c666026627f1546ff28efe88908b2a166f0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:50 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:06 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecc931e2191125378a0a9477c160a961192f08243ea2c2456849e3d27e222e0`  
		Last Modified: Wed, 03 Dec 2025 23:23:08 GMT  
		Size: 8.1 MB (8140516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce9f0fdd9a6972893cb9174962100c606a4ec4f96d43c364367a47626fdf9c`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878cfd957acc34a77a945074318f634f0e69a7c824871f6464251ac78b8a664e`  
		Last Modified: Wed, 03 Dec 2025 23:23:05 GMT  
		Size: 17.6 MB (17560711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff31c3c1cf921e42759f6740e9e0beef431a103e7e0a8d4cc77746069baa2a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57a283bca5c3cafa94cf6aa030b368473a528c61badf87a6acd532479536a3a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 10.2 MB (10195775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d43044fe88440c59cb4d09b26744e4f2a4765098262deecb118d338ea56699`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f15be6ca380c49f5c3b6f9788835a7f811e9ff6921a5c39692cb64255b1572`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2803db336c739715d724a2b06fa65fa1849d95ef8c19e34880c5b5acbc35d88`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f931e0fd6111c2578d5d9a54292a9dfec958fe94d1e7f68f1b31d197a333985`  
		Last Modified: Thu, 04 Dec 2025 00:09:27 GMT  
		Size: 7.2 MB (7230286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc7b8d7478ef5f2f5ba1e5db11c0fc93bd20eafe6b7606d9d47bf2331a2b3c`  
		Last Modified: Thu, 04 Dec 2025 00:09:28 GMT  
		Size: 90.0 KB (89955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d076abb53c41564afd763287157cf740f81e0db1053596ab43b14cd7ef71b07d`  
		Last Modified: Thu, 04 Dec 2025 00:09:25 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a101330bea32635e63394dee524dbef13c06b88980cbb82594b56006da57986`  
		Last Modified: Thu, 04 Dec 2025 00:09:31 GMT  
		Size: 59.9 MB (59893215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc26c05faa4dc67c6281383dfb1b858e05d90847279c446859a199658f586ac2`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdb33cb903b3e7bbad1c970a6cad894a4a031db43544a2245b7413b8146a78f`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:d42c8cf8a28b5613be8a5e682d1f0adc2a66593fc5825c921cbeb79908537a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c000f8f0e671395bd4558756b0240d013b2b9f86f582f6aebdb340e1c0bde`

```dockerfile
```

-	Layers:
	-	`sha256:c8b0bc7a5fcd7022ef2328012ba0f8cd8d24946692ba523f6780c59afcf2c0c5`  
		Last Modified: Thu, 04 Dec 2025 03:07:33 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:3b20b2f3273127bc77b0d5a10d6c89fbe489c6e26aabfcf70374718b183dfaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126234834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30509973b0ac1a4da60db5cd58eafc1683ae159d63618ea8b33fac2fea969ec9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:31 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:32 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935a3faa05b5054eb2d5539416291930c560ec5c5562fc406afa35bd473fb0e6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 7.5 MB (7461370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde152eb030abb1c199a35f2e9e0e6b1b6a57d4feb903df63b11037fac1a2ce6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f06bd5e7fd9b6ded91c70f08fd128821578ffc9820598e8f07b40cfb0d9ce5`  
		Last Modified: Wed, 03 Dec 2025 23:23:55 GMT  
		Size: 17.6 MB (17550088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afc00eecc90cef8da7558059bc5d03c4e8a6fcc711de9e737079165e731684`  
		Last Modified: Wed, 03 Dec 2025 23:23:50 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515c94502ad1a992ad7e0b00b558d157c6f159b4e9db4d9d2f40e7bafb17b92e`  
		Last Modified: Wed, 03 Dec 2025 23:23:52 GMT  
		Size: 10.2 MB (10188522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bee705c92c06181488e34193ffad6a12b619e780a07b1a79299bf5f0145f4d`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a23011c0e0e10c3d92ecd1d44a351ea1c7caa7b8dd85a808ee2e3d7b21fb6f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa197bf85b5aea7f0c51679266daa38199c6e7991b49320c5c16206a14c279f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3c3136863c024060420d7807c203025bc548ac5ad2b0858e446809ab410c`  
		Last Modified: Thu, 04 Dec 2025 00:09:54 GMT  
		Size: 6.5 MB (6538168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f77e8b986e32956581155ff6b177404ce1edb49d73437dd38ef58279f920ef`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 86.4 KB (86396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348c52291ee0284e8483fdfff7481d25d34bb401399ce821ec03bcb55d4d2e94`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018fd645a77660c02db5a21d598961bc1ed40e8aa011a2c6590fef87930aa5e`  
		Last Modified: Thu, 04 Dec 2025 00:09:57 GMT  
		Size: 59.7 MB (59725684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daf7cac083af2912d7cad82e45f8086baaba542e7e0aa6d43a21ce73dff00c`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88842983720a1ed7d8aa571666aff44394345c26366bf0d54590b6ff3eda3a84`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:9960273ea153bbe574b692c69e822b3013ee15f4c6c70e6a909ca44ec1ab3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1927298a387e339d847056a865f7134a8cfc0b73ce2d584fdaf95fa1bc81a8`

```dockerfile
```

-	Layers:
	-	`sha256:6007395b9d82e0ffe5855b313e61375469e3ae796653dc07903f13486fc11870`  
		Last Modified: Thu, 04 Dec 2025 03:07:36 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7c26d2db80935c936465085344b49347e1a3d64aab63c61dde7cb47fb85b0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125991288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb84df0944fb8b77d9caae220f0fe4e6533a8b0bb7ac9d1fe0ab537611d7539`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:fff37f801a284572fb4ec647febb83d21fa848330ad16164593fd754054e4e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eda8b90f0af1ce070ab1b486d36a6f8e52a00099f86dff74b9ede6cbeb4d19c`

```dockerfile
```

-	Layers:
	-	`sha256:7f49d359152acc433dd0182ab053b3a9885e5cbd5434e49990d59ff25fc3a484`  
		Last Modified: Thu, 04 Dec 2025 03:07:40 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:d525718bb067b852a3a33c49485e5f5ac412be1e6e76f7551bdc202d5a889f85
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
$ docker pull docker@sha256:21a1c55469066f188822c840c6524d53ee9839e22016d44ef7fbe33a9cd86d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64714559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19f3c0eff8641da7c2b0ce16d81b1d40c260a23d505336cbec71a4efd465fe7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a151e1882a0ff66dc0af0fe6d18ca20c53f882957b702f02182f533230db9086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239e883311e13240a894908074353c98ca40cc658715597bddde6eab0d29f26`

```dockerfile
```

-	Layers:
	-	`sha256:216ce815280ec2d0835d77acdeab97fbee9288506643bbc7cb64e692fda85d7a`  
		Last Modified: Thu, 04 Dec 2025 03:07:45 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d0265fe0ee552de65a6516d3f06ae73a1653bceec355a4aefe8e354b39c76331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61104123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39a447a955d8f055f4d11bdbd35660231a7f8d130c8074aa02e142c343a3208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:18:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:18:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:18:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:18:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:18:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:18:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:18:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6abcf03c4d2a46ff1f3cf4e321bc7993d4d20b17f12f99d466b39b3555298`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 8.3 MB (8301067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb792a943c4d38855261216162c97e27587aa936e4de5451eeda4d170348a07`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aa1d961beedab5a903eed7b199a7f3cf448a9ad0d235f989735bce0000963`  
		Last Modified: Thu, 04 Dec 2025 01:19:02 GMT  
		Size: 17.6 MB (17560675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136294917ec3532038026ad3f18199c6aff9e645109302b3c9fdc832bf5dd82`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 21.5 MB (21476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0b74dd96a21e6b38324422ba118ccd940a01d181d09275193f948ebd543d2`  
		Last Modified: Thu, 04 Dec 2025 01:19:00 GMT  
		Size: 10.2 MB (10195783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a193c8f7c9fb004babea7c82efc513b5196991d924daf956f6881012fec3`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86d05610e4cf2f79db6d09c9b4c2c8944991a0da701d442726824c5daf33ae`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ebf88cb27a0d9b7e72386749701cbb0df6c753c53caa647578e1151c9f6e0`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc76e87252fb09b02cea86a5b617829392911cde87352fad99dd8bfac4f35cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24448a333caa52a4c783c364a476d2027af604ef74cec044324f6a28724416c5`

```dockerfile
```

-	Layers:
	-	`sha256:4c5c12bece34bf0cfd9182ec595bd154f82fce5392e2d8805658d591a8ddbffe`  
		Last Modified: Thu, 04 Dec 2025 03:07:48 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:935d68f5bf42e536d86f411c2b8a9cedb7cadd4b2e5c4901ed9c19b4f5843297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60072150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ecb3dd3fccd1770e4077f98543a49bb4b3b56dc6c3aa9c2079622abb19001`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:17:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:17:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:17:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:17:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:17:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:17:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:17:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:17:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:17:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab67aee2b47b20a25046ed73de706bd5a80ad82192c27db420a65cfa5fb17cb`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 7.6 MB (7598018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860397c02592909361c994060954f1d684dc0366a2df922a3fe521f02a6b6b2`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ddf54b4c1a081004e3eb1cd154ca1c1cc7e169e416c1ebb9fb23b872919a4d`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 17.6 MB (17550083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645b95707890af1cad5443377a3d8bba32e3701d1f59ee629bd3a1598e45b63`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 21.5 MB (21454910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d968e842fbfa0f7d8d14048d776e945449a586f5772cf04dc12753e58629d9`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 10.2 MB (10188525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482495d52b3d32ead0b4c76816259e750cf45944ac6a48937ed5de349bc73b`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862303f1e616b7c4e5debf343f489e54323b1d7e8d897d6bbcf9951c6fb125e7`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b42590dfec33aa271798a0fdbb5fb080fa6137a58beb89183e43d609cc24`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f53d3adf38731e16863cf838919c725a7485c9343ed47dbe1819cb1eee9fcf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc530b6722d835f222fc005e4ecfc18f010f44d9177c01b8d3fb440e2270eb41`

```dockerfile
```

-	Layers:
	-	`sha256:250e1a2b917f39d22919fc8dfe5a354dcb0d945d2986b1d8ee076e7360e0d189`  
		Last Modified: Thu, 04 Dec 2025 03:07:52 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:05be5900b65fb6922962f3a5cd458bfa73a54fc06caa4147088d27fbcbfbd629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60569466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f578b3c9f73f992024507d6c2ca3b91941f9e7640a6f4d0c06e3abf802ecfcfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:53b87f74f0453103d0e91fd60ae5257848aaf5b69a305e7473eea62bf9dd55b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f007f56500be77ded77125653b2b2062bcf4f13495e20a149611f5435b4cf1e6`

```dockerfile
```

-	Layers:
	-	`sha256:64d865b942bb61e404183343df3b7b76011d6dc7ce17dbb5ea00e4380a7e0293`  
		Last Modified: Thu, 04 Dec 2025 03:07:55 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:d47faf85fc5cb4283d7a20c95b6b02d012250b46ec26567554076e2767cb9093
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
$ docker pull docker@sha256:402b891668de1fe99eb7d054cf25df00a6217232585c02a509ecd7d89ee90856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135884343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b4440e17e983942d30f645a848d94efafacaef8be8733a99feeedc93b05165`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:730e45afac3924277c2d3d65bbd80e18019ece14ae5ca8ec59a55372c9357de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4237c7596712be121f7d034be83210391de8307b0ad7f32c6a82e65b63cd5899`

```dockerfile
```

-	Layers:
	-	`sha256:25e1d1a7097f30c7caefc7d07f5efc216727d9595749698f69ba2d3f3c9ac6ce`  
		Last Modified: Thu, 04 Dec 2025 03:07:31 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:fe601bbe28b63642b9b52b7a8478c09ad9007efb3307344dd0200e78ec89757d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128099244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11f21ae0c179baf1e0e49afea4c0c666026627f1546ff28efe88908b2a166f0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:50 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:06 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecc931e2191125378a0a9477c160a961192f08243ea2c2456849e3d27e222e0`  
		Last Modified: Wed, 03 Dec 2025 23:23:08 GMT  
		Size: 8.1 MB (8140516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce9f0fdd9a6972893cb9174962100c606a4ec4f96d43c364367a47626fdf9c`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878cfd957acc34a77a945074318f634f0e69a7c824871f6464251ac78b8a664e`  
		Last Modified: Wed, 03 Dec 2025 23:23:05 GMT  
		Size: 17.6 MB (17560711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff31c3c1cf921e42759f6740e9e0beef431a103e7e0a8d4cc77746069baa2a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57a283bca5c3cafa94cf6aa030b368473a528c61badf87a6acd532479536a3a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 10.2 MB (10195775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d43044fe88440c59cb4d09b26744e4f2a4765098262deecb118d338ea56699`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f15be6ca380c49f5c3b6f9788835a7f811e9ff6921a5c39692cb64255b1572`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2803db336c739715d724a2b06fa65fa1849d95ef8c19e34880c5b5acbc35d88`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f931e0fd6111c2578d5d9a54292a9dfec958fe94d1e7f68f1b31d197a333985`  
		Last Modified: Thu, 04 Dec 2025 00:09:27 GMT  
		Size: 7.2 MB (7230286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc7b8d7478ef5f2f5ba1e5db11c0fc93bd20eafe6b7606d9d47bf2331a2b3c`  
		Last Modified: Thu, 04 Dec 2025 00:09:28 GMT  
		Size: 90.0 KB (89955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d076abb53c41564afd763287157cf740f81e0db1053596ab43b14cd7ef71b07d`  
		Last Modified: Thu, 04 Dec 2025 00:09:25 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a101330bea32635e63394dee524dbef13c06b88980cbb82594b56006da57986`  
		Last Modified: Thu, 04 Dec 2025 00:09:31 GMT  
		Size: 59.9 MB (59893215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc26c05faa4dc67c6281383dfb1b858e05d90847279c446859a199658f586ac2`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdb33cb903b3e7bbad1c970a6cad894a4a031db43544a2245b7413b8146a78f`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d42c8cf8a28b5613be8a5e682d1f0adc2a66593fc5825c921cbeb79908537a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c000f8f0e671395bd4558756b0240d013b2b9f86f582f6aebdb340e1c0bde`

```dockerfile
```

-	Layers:
	-	`sha256:c8b0bc7a5fcd7022ef2328012ba0f8cd8d24946692ba523f6780c59afcf2c0c5`  
		Last Modified: Thu, 04 Dec 2025 03:07:33 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:3b20b2f3273127bc77b0d5a10d6c89fbe489c6e26aabfcf70374718b183dfaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126234834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30509973b0ac1a4da60db5cd58eafc1683ae159d63618ea8b33fac2fea969ec9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:31 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:32 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935a3faa05b5054eb2d5539416291930c560ec5c5562fc406afa35bd473fb0e6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 7.5 MB (7461370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde152eb030abb1c199a35f2e9e0e6b1b6a57d4feb903df63b11037fac1a2ce6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f06bd5e7fd9b6ded91c70f08fd128821578ffc9820598e8f07b40cfb0d9ce5`  
		Last Modified: Wed, 03 Dec 2025 23:23:55 GMT  
		Size: 17.6 MB (17550088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afc00eecc90cef8da7558059bc5d03c4e8a6fcc711de9e737079165e731684`  
		Last Modified: Wed, 03 Dec 2025 23:23:50 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515c94502ad1a992ad7e0b00b558d157c6f159b4e9db4d9d2f40e7bafb17b92e`  
		Last Modified: Wed, 03 Dec 2025 23:23:52 GMT  
		Size: 10.2 MB (10188522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bee705c92c06181488e34193ffad6a12b619e780a07b1a79299bf5f0145f4d`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a23011c0e0e10c3d92ecd1d44a351ea1c7caa7b8dd85a808ee2e3d7b21fb6f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa197bf85b5aea7f0c51679266daa38199c6e7991b49320c5c16206a14c279f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3c3136863c024060420d7807c203025bc548ac5ad2b0858e446809ab410c`  
		Last Modified: Thu, 04 Dec 2025 00:09:54 GMT  
		Size: 6.5 MB (6538168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f77e8b986e32956581155ff6b177404ce1edb49d73437dd38ef58279f920ef`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 86.4 KB (86396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348c52291ee0284e8483fdfff7481d25d34bb401399ce821ec03bcb55d4d2e94`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018fd645a77660c02db5a21d598961bc1ed40e8aa011a2c6590fef87930aa5e`  
		Last Modified: Thu, 04 Dec 2025 00:09:57 GMT  
		Size: 59.7 MB (59725684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daf7cac083af2912d7cad82e45f8086baaba542e7e0aa6d43a21ce73dff00c`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88842983720a1ed7d8aa571666aff44394345c26366bf0d54590b6ff3eda3a84`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9960273ea153bbe574b692c69e822b3013ee15f4c6c70e6a909ca44ec1ab3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1927298a387e339d847056a865f7134a8cfc0b73ce2d584fdaf95fa1bc81a8`

```dockerfile
```

-	Layers:
	-	`sha256:6007395b9d82e0ffe5855b313e61375469e3ae796653dc07903f13486fc11870`  
		Last Modified: Thu, 04 Dec 2025 03:07:36 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7c26d2db80935c936465085344b49347e1a3d64aab63c61dde7cb47fb85b0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125991288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb84df0944fb8b77d9caae220f0fe4e6533a8b0bb7ac9d1fe0ab537611d7539`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fff37f801a284572fb4ec647febb83d21fa848330ad16164593fd754054e4e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eda8b90f0af1ce070ab1b486d36a6f8e52a00099f86dff74b9ede6cbeb4d19c`

```dockerfile
```

-	Layers:
	-	`sha256:7f49d359152acc433dd0182ab053b3a9885e5cbd5434e49990d59ff25fc3a484`  
		Last Modified: Thu, 04 Dec 2025 03:07:40 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:421dffbe324135321070051128d9d2787f0465a94d728070953b89255438a5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:353a1727d0e6ac8343824427ff6d442390472e0bb77ca01655da0ddcf51fb9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156655034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfdf4d733c409824955ff98bc575e0384deb01f66c4f8e9a244e158f749ea1f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
# Thu, 04 Dec 2025 00:34:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 00:34:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 00:34:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 00:34:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91aa056e56aa4a66ab4445fc928d9900f02526039d0d9e034dbd5f1864ded0e`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 3.4 MB (3398378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ba6b907925696d4f4bf8e90017155cfc57c2eb3a3daf7b148f8e03ec3e6e46`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa8d4bd6998c2fe7060be7b4c380915afb0718f2a048cffec66cfa2b3396679`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb4f0a9a116b4469861628ca4fa5396cf4046b9589a4d19291e11bfea5fc4c6`  
		Last Modified: Thu, 04 Dec 2025 00:34:49 GMT  
		Size: 17.4 MB (17370975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0121931059414c5b535a820a06149e50072743b8d7d9d1292e94b5dd7cde587f`  
		Last Modified: Thu, 04 Dec 2025 00:34:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4b08832b0e539cc368981d37d867659cadd73c07d5b17094e24239509d6d408f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2014725d32624c20c843af1525ac27aa85a87442225e3a832e40bb9658fa40`

```dockerfile
```

-	Layers:
	-	`sha256:d430a287400d6e64aca730c1235ea91292ca5733da9bb24288faf42078d9d405`  
		Last Modified: Thu, 04 Dec 2025 03:07:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a1db98f222784429b330f778f1957ad3018c290fa95637335ca9ee58c09bd1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147091297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c01b600ca0f7971b32388b10745a1245988aa3e8ca83212a3ea4c2b2eb9609c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
# Thu, 04 Dec 2025 00:34:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 00:34:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 00:34:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 00:34:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29744f0d4e84a604abd643d72e500a942b93b47aebc9608aeb11c9547505978f`  
		Last Modified: Thu, 04 Dec 2025 00:34:30 GMT  
		Size: 3.4 MB (3389949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd8dfe81186ff0b816407ebca7cde7473e4568a00053e41a9b865506bb318b0`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334d36e8d2a2055d1ce374a4db658c40f1524af962083d9b5da52852d76a46cd`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0acb58cf5a910482ee59a629e47ddf2882796d6846f7fcba3860c753046c3`  
		Last Modified: Thu, 04 Dec 2025 00:34:29 GMT  
		Size: 17.7 MB (17708720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68ee96465b587d4e1d201671d6f38af93ce12e3e8de1e4318ce20a9a3a22aa5`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:629ac163c9e7113117c78d53db8ab7c25aba4ee3de17c2844199d515d03b1900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63d85a6970c712972dadb4c3f5562f4814c08c63e23177be3b9fb30441e0646`

```dockerfile
```

-	Layers:
	-	`sha256:a9a45b6a9af3185edc3fef012c4ee2bbc1e2310c25a9b46260487d287c102821`  
		Last Modified: Thu, 04 Dec 2025 03:08:01 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:0eb975351ee9df33c41e2946cbd2143ba55fac8ae27c448d9b3fdbd060e969a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:dcd91f0a9029b88613dc48540fe8c128b08bff07dd8b99f4f0242513176f5297
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3290731333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799920065e3e5f973ef96625fe4937bc2563ef5a8e33a59bcf9de238cabe02f5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 23:27:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:45 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:19 GMT
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
	-	`sha256:d7146b17b5860acc8808e415263a03814888a80daaac674aad997e45e4815684`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcde76394ea2b592fadc80c106462452d55b0d2db294199cd06e6368a24364c`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 399.7 KB (399722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620bb71f2687fad09692e4f84af86fcfcccd93276ea8697e98e13c65e534b9c3`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465405d75d81f743b9557eef457a787436466226d68ca5613d82a7c0b02a84d2`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07117c52ec04e5430ba6c16b89755a395af5dc950c1e1965c1522e0b6c7c9369`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 19.5 MB (19450943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3e1dd17fe0599cd773fe8876a3468ed2785a46b58b877ece7fd1b58b174a22`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb064c05a6de4303a29f355e360b69a0b4018d7f54aadc58e85ed89554d726c`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986e5dffed43d7b98b12e2629e4811443a52b3b642ca30a1a9cd58487af9617`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b3176876e2fd382f76e0a0f989cf351e47e43b0507d7e9d91f5846ac99ea9`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 23.9 MB (23949262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591161397992bd49794d31aa33971c487096caccf147b7786c1e0a755a9fe805`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5d7df70beef98e61be396a7a9c43f445629c0394d49ad6b7245913efaf99a2`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e81f136de465956899822ab4c68c183a31a5a4568f59543513268a0cd87b4`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c959e0b45832e9394f8ced26f7a951cfa65a205041622a521e760b10428ac80`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 11.5 MB (11463861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:e510d0ffbc8c058424c173f9fdc8cf04cc404418596a5affa555804099d86454
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1825263813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f07aa98e515049fbc2b1e495db11a4b0d477c90d0af1e624c7091898258e4fa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Wed, 03 Dec 2025 23:27:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:29 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:28:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:28:55 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:22 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:37 GMT
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
	-	`sha256:f95ab1d322f7331427de0527a98516714be5fdfab8001a0c3afbfdd375f8c704`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997dee9e9b12bed5bc50b78d9d4a23fa986d3c820f38741c6df0273e145b4228`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 501.4 KB (501396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8221a12dd08308b3b8cd4120faa67fcdef9df7d39a4a7acd1474ee4b616290`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88be20e3446295169e1821cf2636d87b5284dd5ea89d65f2b8d6928855ae5b8`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8279728faba290f6ba2b243e3e21a5a11dec89f4ef7ce8e21bc6efb45beb59`  
		Last Modified: Wed, 03 Dec 2025 23:41:22 GMT  
		Size: 19.4 MB (19424449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0ef6633566397de87875a06aae522041d6e3b3a4004ac25a21f129c00b741f`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a349148f8226a779c9bac7fe27b9bb6662d9f5d28cb22d5969722e7e79b280`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4c28f07a327eb3afb667f83caa8e98c39382dcf476cbc17b52e84e0a43092b`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6508f164b53e8ff2ae3c44be363df93cbfcb58724fadaeae0c3dc1170b3acd`  
		Last Modified: Wed, 03 Dec 2025 23:41:23 GMT  
		Size: 23.9 MB (23925342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb3468481b597bde6c2cf074d7b9737c7a77424f16922fbc386ea348e80025`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f80013208797c388923aa4d38cbea4495d3ea0c614ed53a2293f41f22d21a84`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187a71b662b80ffd9fe1339b7e7d5cbff0079de921771aac208a9b839ae48b2`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be497084a394b66ecc710847dddcef4176a5a319c37cb4b40d904e72c8c9a5`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 11.4 MB (11439399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:983813a6983c58f428973a22873ce9e8091209be5490d03e1b2b1a61196967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:e510d0ffbc8c058424c173f9fdc8cf04cc404418596a5affa555804099d86454
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1825263813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f07aa98e515049fbc2b1e495db11a4b0d477c90d0af1e624c7091898258e4fa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Wed, 03 Dec 2025 23:27:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:29 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:28:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:28:55 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:22 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:37 GMT
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
	-	`sha256:f95ab1d322f7331427de0527a98516714be5fdfab8001a0c3afbfdd375f8c704`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997dee9e9b12bed5bc50b78d9d4a23fa986d3c820f38741c6df0273e145b4228`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 501.4 KB (501396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8221a12dd08308b3b8cd4120faa67fcdef9df7d39a4a7acd1474ee4b616290`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88be20e3446295169e1821cf2636d87b5284dd5ea89d65f2b8d6928855ae5b8`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8279728faba290f6ba2b243e3e21a5a11dec89f4ef7ce8e21bc6efb45beb59`  
		Last Modified: Wed, 03 Dec 2025 23:41:22 GMT  
		Size: 19.4 MB (19424449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0ef6633566397de87875a06aae522041d6e3b3a4004ac25a21f129c00b741f`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a349148f8226a779c9bac7fe27b9bb6662d9f5d28cb22d5969722e7e79b280`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4c28f07a327eb3afb667f83caa8e98c39382dcf476cbc17b52e84e0a43092b`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6508f164b53e8ff2ae3c44be363df93cbfcb58724fadaeae0c3dc1170b3acd`  
		Last Modified: Wed, 03 Dec 2025 23:41:23 GMT  
		Size: 23.9 MB (23925342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb3468481b597bde6c2cf074d7b9737c7a77424f16922fbc386ea348e80025`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f80013208797c388923aa4d38cbea4495d3ea0c614ed53a2293f41f22d21a84`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187a71b662b80ffd9fe1339b7e7d5cbff0079de921771aac208a9b839ae48b2`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be497084a394b66ecc710847dddcef4176a5a319c37cb4b40d904e72c8c9a5`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 11.4 MB (11439399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:2d936418a8c21ad8678fc7b3af4cbb724a2ea1347653cbac3ad6603facd89118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:dcd91f0a9029b88613dc48540fe8c128b08bff07dd8b99f4f0242513176f5297
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3290731333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799920065e3e5f973ef96625fe4937bc2563ef5a8e33a59bcf9de238cabe02f5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 23:27:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:45 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:19 GMT
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
	-	`sha256:d7146b17b5860acc8808e415263a03814888a80daaac674aad997e45e4815684`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcde76394ea2b592fadc80c106462452d55b0d2db294199cd06e6368a24364c`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 399.7 KB (399722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620bb71f2687fad09692e4f84af86fcfcccd93276ea8697e98e13c65e534b9c3`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465405d75d81f743b9557eef457a787436466226d68ca5613d82a7c0b02a84d2`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07117c52ec04e5430ba6c16b89755a395af5dc950c1e1965c1522e0b6c7c9369`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 19.5 MB (19450943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3e1dd17fe0599cd773fe8876a3468ed2785a46b58b877ece7fd1b58b174a22`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb064c05a6de4303a29f355e360b69a0b4018d7f54aadc58e85ed89554d726c`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986e5dffed43d7b98b12e2629e4811443a52b3b642ca30a1a9cd58487af9617`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b3176876e2fd382f76e0a0f989cf351e47e43b0507d7e9d91f5846ac99ea9`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 23.9 MB (23949262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591161397992bd49794d31aa33971c487096caccf147b7786c1e0a755a9fe805`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5d7df70beef98e61be396a7a9c43f445629c0394d49ad6b7245913efaf99a2`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e81f136de465956899822ab4c68c183a31a5a4568f59543513268a0cd87b4`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c959e0b45832e9394f8ced26f7a951cfa65a205041622a521e760b10428ac80`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 11.5 MB (11463861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1`

```console
$ docker pull docker@sha256:d47faf85fc5cb4283d7a20c95b6b02d012250b46ec26567554076e2767cb9093
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

### `docker:29.1` - linux; amd64

```console
$ docker pull docker@sha256:402b891668de1fe99eb7d054cf25df00a6217232585c02a509ecd7d89ee90856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135884343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b4440e17e983942d30f645a848d94efafacaef8be8733a99feeedc93b05165`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:730e45afac3924277c2d3d65bbd80e18019ece14ae5ca8ec59a55372c9357de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4237c7596712be121f7d034be83210391de8307b0ad7f32c6a82e65b63cd5899`

```dockerfile
```

-	Layers:
	-	`sha256:25e1d1a7097f30c7caefc7d07f5efc216727d9595749698f69ba2d3f3c9ac6ce`  
		Last Modified: Thu, 04 Dec 2025 03:07:31 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:fe601bbe28b63642b9b52b7a8478c09ad9007efb3307344dd0200e78ec89757d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128099244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11f21ae0c179baf1e0e49afea4c0c666026627f1546ff28efe88908b2a166f0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:50 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:06 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecc931e2191125378a0a9477c160a961192f08243ea2c2456849e3d27e222e0`  
		Last Modified: Wed, 03 Dec 2025 23:23:08 GMT  
		Size: 8.1 MB (8140516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce9f0fdd9a6972893cb9174962100c606a4ec4f96d43c364367a47626fdf9c`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878cfd957acc34a77a945074318f634f0e69a7c824871f6464251ac78b8a664e`  
		Last Modified: Wed, 03 Dec 2025 23:23:05 GMT  
		Size: 17.6 MB (17560711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff31c3c1cf921e42759f6740e9e0beef431a103e7e0a8d4cc77746069baa2a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57a283bca5c3cafa94cf6aa030b368473a528c61badf87a6acd532479536a3a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 10.2 MB (10195775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d43044fe88440c59cb4d09b26744e4f2a4765098262deecb118d338ea56699`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f15be6ca380c49f5c3b6f9788835a7f811e9ff6921a5c39692cb64255b1572`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2803db336c739715d724a2b06fa65fa1849d95ef8c19e34880c5b5acbc35d88`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f931e0fd6111c2578d5d9a54292a9dfec958fe94d1e7f68f1b31d197a333985`  
		Last Modified: Thu, 04 Dec 2025 00:09:27 GMT  
		Size: 7.2 MB (7230286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc7b8d7478ef5f2f5ba1e5db11c0fc93bd20eafe6b7606d9d47bf2331a2b3c`  
		Last Modified: Thu, 04 Dec 2025 00:09:28 GMT  
		Size: 90.0 KB (89955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d076abb53c41564afd763287157cf740f81e0db1053596ab43b14cd7ef71b07d`  
		Last Modified: Thu, 04 Dec 2025 00:09:25 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a101330bea32635e63394dee524dbef13c06b88980cbb82594b56006da57986`  
		Last Modified: Thu, 04 Dec 2025 00:09:31 GMT  
		Size: 59.9 MB (59893215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc26c05faa4dc67c6281383dfb1b858e05d90847279c446859a199658f586ac2`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdb33cb903b3e7bbad1c970a6cad894a4a031db43544a2245b7413b8146a78f`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:d42c8cf8a28b5613be8a5e682d1f0adc2a66593fc5825c921cbeb79908537a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c000f8f0e671395bd4558756b0240d013b2b9f86f582f6aebdb340e1c0bde`

```dockerfile
```

-	Layers:
	-	`sha256:c8b0bc7a5fcd7022ef2328012ba0f8cd8d24946692ba523f6780c59afcf2c0c5`  
		Last Modified: Thu, 04 Dec 2025 03:07:33 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:3b20b2f3273127bc77b0d5a10d6c89fbe489c6e26aabfcf70374718b183dfaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126234834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30509973b0ac1a4da60db5cd58eafc1683ae159d63618ea8b33fac2fea969ec9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:31 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:32 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935a3faa05b5054eb2d5539416291930c560ec5c5562fc406afa35bd473fb0e6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 7.5 MB (7461370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde152eb030abb1c199a35f2e9e0e6b1b6a57d4feb903df63b11037fac1a2ce6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f06bd5e7fd9b6ded91c70f08fd128821578ffc9820598e8f07b40cfb0d9ce5`  
		Last Modified: Wed, 03 Dec 2025 23:23:55 GMT  
		Size: 17.6 MB (17550088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afc00eecc90cef8da7558059bc5d03c4e8a6fcc711de9e737079165e731684`  
		Last Modified: Wed, 03 Dec 2025 23:23:50 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515c94502ad1a992ad7e0b00b558d157c6f159b4e9db4d9d2f40e7bafb17b92e`  
		Last Modified: Wed, 03 Dec 2025 23:23:52 GMT  
		Size: 10.2 MB (10188522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bee705c92c06181488e34193ffad6a12b619e780a07b1a79299bf5f0145f4d`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a23011c0e0e10c3d92ecd1d44a351ea1c7caa7b8dd85a808ee2e3d7b21fb6f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa197bf85b5aea7f0c51679266daa38199c6e7991b49320c5c16206a14c279f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3c3136863c024060420d7807c203025bc548ac5ad2b0858e446809ab410c`  
		Last Modified: Thu, 04 Dec 2025 00:09:54 GMT  
		Size: 6.5 MB (6538168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f77e8b986e32956581155ff6b177404ce1edb49d73437dd38ef58279f920ef`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 86.4 KB (86396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348c52291ee0284e8483fdfff7481d25d34bb401399ce821ec03bcb55d4d2e94`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018fd645a77660c02db5a21d598961bc1ed40e8aa011a2c6590fef87930aa5e`  
		Last Modified: Thu, 04 Dec 2025 00:09:57 GMT  
		Size: 59.7 MB (59725684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daf7cac083af2912d7cad82e45f8086baaba542e7e0aa6d43a21ce73dff00c`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88842983720a1ed7d8aa571666aff44394345c26366bf0d54590b6ff3eda3a84`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:9960273ea153bbe574b692c69e822b3013ee15f4c6c70e6a909ca44ec1ab3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1927298a387e339d847056a865f7134a8cfc0b73ce2d584fdaf95fa1bc81a8`

```dockerfile
```

-	Layers:
	-	`sha256:6007395b9d82e0ffe5855b313e61375469e3ae796653dc07903f13486fc11870`  
		Last Modified: Thu, 04 Dec 2025 03:07:36 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7c26d2db80935c936465085344b49347e1a3d64aab63c61dde7cb47fb85b0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125991288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb84df0944fb8b77d9caae220f0fe4e6533a8b0bb7ac9d1fe0ab537611d7539`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:fff37f801a284572fb4ec647febb83d21fa848330ad16164593fd754054e4e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eda8b90f0af1ce070ab1b486d36a6f8e52a00099f86dff74b9ede6cbeb4d19c`

```dockerfile
```

-	Layers:
	-	`sha256:7f49d359152acc433dd0182ab053b3a9885e5cbd5434e49990d59ff25fc3a484`  
		Last Modified: Thu, 04 Dec 2025 03:07:40 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-cli`

```console
$ docker pull docker@sha256:d525718bb067b852a3a33c49485e5f5ac412be1e6e76f7551bdc202d5a889f85
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

### `docker:29.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:21a1c55469066f188822c840c6524d53ee9839e22016d44ef7fbe33a9cd86d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64714559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19f3c0eff8641da7c2b0ce16d81b1d40c260a23d505336cbec71a4efd465fe7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a151e1882a0ff66dc0af0fe6d18ca20c53f882957b702f02182f533230db9086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239e883311e13240a894908074353c98ca40cc658715597bddde6eab0d29f26`

```dockerfile
```

-	Layers:
	-	`sha256:216ce815280ec2d0835d77acdeab97fbee9288506643bbc7cb64e692fda85d7a`  
		Last Modified: Thu, 04 Dec 2025 03:07:45 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d0265fe0ee552de65a6516d3f06ae73a1653bceec355a4aefe8e354b39c76331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61104123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39a447a955d8f055f4d11bdbd35660231a7f8d130c8074aa02e142c343a3208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:18:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:18:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:18:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:18:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:18:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:18:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:18:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6abcf03c4d2a46ff1f3cf4e321bc7993d4d20b17f12f99d466b39b3555298`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 8.3 MB (8301067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb792a943c4d38855261216162c97e27587aa936e4de5451eeda4d170348a07`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aa1d961beedab5a903eed7b199a7f3cf448a9ad0d235f989735bce0000963`  
		Last Modified: Thu, 04 Dec 2025 01:19:02 GMT  
		Size: 17.6 MB (17560675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136294917ec3532038026ad3f18199c6aff9e645109302b3c9fdc832bf5dd82`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 21.5 MB (21476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0b74dd96a21e6b38324422ba118ccd940a01d181d09275193f948ebd543d2`  
		Last Modified: Thu, 04 Dec 2025 01:19:00 GMT  
		Size: 10.2 MB (10195783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a193c8f7c9fb004babea7c82efc513b5196991d924daf956f6881012fec3`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86d05610e4cf2f79db6d09c9b4c2c8944991a0da701d442726824c5daf33ae`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ebf88cb27a0d9b7e72386749701cbb0df6c753c53caa647578e1151c9f6e0`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc76e87252fb09b02cea86a5b617829392911cde87352fad99dd8bfac4f35cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24448a333caa52a4c783c364a476d2027af604ef74cec044324f6a28724416c5`

```dockerfile
```

-	Layers:
	-	`sha256:4c5c12bece34bf0cfd9182ec595bd154f82fce5392e2d8805658d591a8ddbffe`  
		Last Modified: Thu, 04 Dec 2025 03:07:48 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:935d68f5bf42e536d86f411c2b8a9cedb7cadd4b2e5c4901ed9c19b4f5843297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60072150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ecb3dd3fccd1770e4077f98543a49bb4b3b56dc6c3aa9c2079622abb19001`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:17:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:17:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:17:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:17:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:17:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:17:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:17:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:17:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:17:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab67aee2b47b20a25046ed73de706bd5a80ad82192c27db420a65cfa5fb17cb`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 7.6 MB (7598018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860397c02592909361c994060954f1d684dc0366a2df922a3fe521f02a6b6b2`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ddf54b4c1a081004e3eb1cd154ca1c1cc7e169e416c1ebb9fb23b872919a4d`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 17.6 MB (17550083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645b95707890af1cad5443377a3d8bba32e3701d1f59ee629bd3a1598e45b63`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 21.5 MB (21454910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d968e842fbfa0f7d8d14048d776e945449a586f5772cf04dc12753e58629d9`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 10.2 MB (10188525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482495d52b3d32ead0b4c76816259e750cf45944ac6a48937ed5de349bc73b`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862303f1e616b7c4e5debf343f489e54323b1d7e8d897d6bbcf9951c6fb125e7`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b42590dfec33aa271798a0fdbb5fb080fa6137a58beb89183e43d609cc24`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f53d3adf38731e16863cf838919c725a7485c9343ed47dbe1819cb1eee9fcf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc530b6722d835f222fc005e4ecfc18f010f44d9177c01b8d3fb440e2270eb41`

```dockerfile
```

-	Layers:
	-	`sha256:250e1a2b917f39d22919fc8dfe5a354dcb0d945d2986b1d8ee076e7360e0d189`  
		Last Modified: Thu, 04 Dec 2025 03:07:52 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:05be5900b65fb6922962f3a5cd458bfa73a54fc06caa4147088d27fbcbfbd629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60569466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f578b3c9f73f992024507d6c2ca3b91941f9e7640a6f4d0c06e3abf802ecfcfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:53b87f74f0453103d0e91fd60ae5257848aaf5b69a305e7473eea62bf9dd55b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f007f56500be77ded77125653b2b2062bcf4f13495e20a149611f5435b4cf1e6`

```dockerfile
```

-	Layers:
	-	`sha256:64d865b942bb61e404183343df3b7b76011d6dc7ce17dbb5ea00e4380a7e0293`  
		Last Modified: Thu, 04 Dec 2025 03:07:55 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-dind`

```console
$ docker pull docker@sha256:d47faf85fc5cb4283d7a20c95b6b02d012250b46ec26567554076e2767cb9093
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

### `docker:29.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:402b891668de1fe99eb7d054cf25df00a6217232585c02a509ecd7d89ee90856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135884343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b4440e17e983942d30f645a848d94efafacaef8be8733a99feeedc93b05165`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:730e45afac3924277c2d3d65bbd80e18019ece14ae5ca8ec59a55372c9357de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4237c7596712be121f7d034be83210391de8307b0ad7f32c6a82e65b63cd5899`

```dockerfile
```

-	Layers:
	-	`sha256:25e1d1a7097f30c7caefc7d07f5efc216727d9595749698f69ba2d3f3c9ac6ce`  
		Last Modified: Thu, 04 Dec 2025 03:07:31 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:fe601bbe28b63642b9b52b7a8478c09ad9007efb3307344dd0200e78ec89757d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128099244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11f21ae0c179baf1e0e49afea4c0c666026627f1546ff28efe88908b2a166f0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:50 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:06 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecc931e2191125378a0a9477c160a961192f08243ea2c2456849e3d27e222e0`  
		Last Modified: Wed, 03 Dec 2025 23:23:08 GMT  
		Size: 8.1 MB (8140516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce9f0fdd9a6972893cb9174962100c606a4ec4f96d43c364367a47626fdf9c`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878cfd957acc34a77a945074318f634f0e69a7c824871f6464251ac78b8a664e`  
		Last Modified: Wed, 03 Dec 2025 23:23:05 GMT  
		Size: 17.6 MB (17560711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff31c3c1cf921e42759f6740e9e0beef431a103e7e0a8d4cc77746069baa2a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57a283bca5c3cafa94cf6aa030b368473a528c61badf87a6acd532479536a3a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 10.2 MB (10195775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d43044fe88440c59cb4d09b26744e4f2a4765098262deecb118d338ea56699`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f15be6ca380c49f5c3b6f9788835a7f811e9ff6921a5c39692cb64255b1572`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2803db336c739715d724a2b06fa65fa1849d95ef8c19e34880c5b5acbc35d88`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f931e0fd6111c2578d5d9a54292a9dfec958fe94d1e7f68f1b31d197a333985`  
		Last Modified: Thu, 04 Dec 2025 00:09:27 GMT  
		Size: 7.2 MB (7230286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc7b8d7478ef5f2f5ba1e5db11c0fc93bd20eafe6b7606d9d47bf2331a2b3c`  
		Last Modified: Thu, 04 Dec 2025 00:09:28 GMT  
		Size: 90.0 KB (89955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d076abb53c41564afd763287157cf740f81e0db1053596ab43b14cd7ef71b07d`  
		Last Modified: Thu, 04 Dec 2025 00:09:25 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a101330bea32635e63394dee524dbef13c06b88980cbb82594b56006da57986`  
		Last Modified: Thu, 04 Dec 2025 00:09:31 GMT  
		Size: 59.9 MB (59893215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc26c05faa4dc67c6281383dfb1b858e05d90847279c446859a199658f586ac2`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdb33cb903b3e7bbad1c970a6cad894a4a031db43544a2245b7413b8146a78f`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d42c8cf8a28b5613be8a5e682d1f0adc2a66593fc5825c921cbeb79908537a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c000f8f0e671395bd4558756b0240d013b2b9f86f582f6aebdb340e1c0bde`

```dockerfile
```

-	Layers:
	-	`sha256:c8b0bc7a5fcd7022ef2328012ba0f8cd8d24946692ba523f6780c59afcf2c0c5`  
		Last Modified: Thu, 04 Dec 2025 03:07:33 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:3b20b2f3273127bc77b0d5a10d6c89fbe489c6e26aabfcf70374718b183dfaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126234834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30509973b0ac1a4da60db5cd58eafc1683ae159d63618ea8b33fac2fea969ec9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:31 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:32 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935a3faa05b5054eb2d5539416291930c560ec5c5562fc406afa35bd473fb0e6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 7.5 MB (7461370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde152eb030abb1c199a35f2e9e0e6b1b6a57d4feb903df63b11037fac1a2ce6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f06bd5e7fd9b6ded91c70f08fd128821578ffc9820598e8f07b40cfb0d9ce5`  
		Last Modified: Wed, 03 Dec 2025 23:23:55 GMT  
		Size: 17.6 MB (17550088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afc00eecc90cef8da7558059bc5d03c4e8a6fcc711de9e737079165e731684`  
		Last Modified: Wed, 03 Dec 2025 23:23:50 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515c94502ad1a992ad7e0b00b558d157c6f159b4e9db4d9d2f40e7bafb17b92e`  
		Last Modified: Wed, 03 Dec 2025 23:23:52 GMT  
		Size: 10.2 MB (10188522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bee705c92c06181488e34193ffad6a12b619e780a07b1a79299bf5f0145f4d`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a23011c0e0e10c3d92ecd1d44a351ea1c7caa7b8dd85a808ee2e3d7b21fb6f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa197bf85b5aea7f0c51679266daa38199c6e7991b49320c5c16206a14c279f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3c3136863c024060420d7807c203025bc548ac5ad2b0858e446809ab410c`  
		Last Modified: Thu, 04 Dec 2025 00:09:54 GMT  
		Size: 6.5 MB (6538168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f77e8b986e32956581155ff6b177404ce1edb49d73437dd38ef58279f920ef`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 86.4 KB (86396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348c52291ee0284e8483fdfff7481d25d34bb401399ce821ec03bcb55d4d2e94`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018fd645a77660c02db5a21d598961bc1ed40e8aa011a2c6590fef87930aa5e`  
		Last Modified: Thu, 04 Dec 2025 00:09:57 GMT  
		Size: 59.7 MB (59725684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daf7cac083af2912d7cad82e45f8086baaba542e7e0aa6d43a21ce73dff00c`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88842983720a1ed7d8aa571666aff44394345c26366bf0d54590b6ff3eda3a84`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9960273ea153bbe574b692c69e822b3013ee15f4c6c70e6a909ca44ec1ab3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1927298a387e339d847056a865f7134a8cfc0b73ce2d584fdaf95fa1bc81a8`

```dockerfile
```

-	Layers:
	-	`sha256:6007395b9d82e0ffe5855b313e61375469e3ae796653dc07903f13486fc11870`  
		Last Modified: Thu, 04 Dec 2025 03:07:36 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7c26d2db80935c936465085344b49347e1a3d64aab63c61dde7cb47fb85b0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125991288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb84df0944fb8b77d9caae220f0fe4e6533a8b0bb7ac9d1fe0ab537611d7539`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fff37f801a284572fb4ec647febb83d21fa848330ad16164593fd754054e4e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eda8b90f0af1ce070ab1b486d36a6f8e52a00099f86dff74b9ede6cbeb4d19c`

```dockerfile
```

-	Layers:
	-	`sha256:7f49d359152acc433dd0182ab053b3a9885e5cbd5434e49990d59ff25fc3a484`  
		Last Modified: Thu, 04 Dec 2025 03:07:40 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-dind-rootless`

```console
$ docker pull docker@sha256:421dffbe324135321070051128d9d2787f0465a94d728070953b89255438a5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:353a1727d0e6ac8343824427ff6d442390472e0bb77ca01655da0ddcf51fb9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156655034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfdf4d733c409824955ff98bc575e0384deb01f66c4f8e9a244e158f749ea1f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
# Thu, 04 Dec 2025 00:34:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 00:34:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 00:34:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 00:34:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91aa056e56aa4a66ab4445fc928d9900f02526039d0d9e034dbd5f1864ded0e`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 3.4 MB (3398378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ba6b907925696d4f4bf8e90017155cfc57c2eb3a3daf7b148f8e03ec3e6e46`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa8d4bd6998c2fe7060be7b4c380915afb0718f2a048cffec66cfa2b3396679`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb4f0a9a116b4469861628ca4fa5396cf4046b9589a4d19291e11bfea5fc4c6`  
		Last Modified: Thu, 04 Dec 2025 00:34:49 GMT  
		Size: 17.4 MB (17370975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0121931059414c5b535a820a06149e50072743b8d7d9d1292e94b5dd7cde587f`  
		Last Modified: Thu, 04 Dec 2025 00:34:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4b08832b0e539cc368981d37d867659cadd73c07d5b17094e24239509d6d408f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2014725d32624c20c843af1525ac27aa85a87442225e3a832e40bb9658fa40`

```dockerfile
```

-	Layers:
	-	`sha256:d430a287400d6e64aca730c1235ea91292ca5733da9bb24288faf42078d9d405`  
		Last Modified: Thu, 04 Dec 2025 03:07:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a1db98f222784429b330f778f1957ad3018c290fa95637335ca9ee58c09bd1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147091297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c01b600ca0f7971b32388b10745a1245988aa3e8ca83212a3ea4c2b2eb9609c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
# Thu, 04 Dec 2025 00:34:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 00:34:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 00:34:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 00:34:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29744f0d4e84a604abd643d72e500a942b93b47aebc9608aeb11c9547505978f`  
		Last Modified: Thu, 04 Dec 2025 00:34:30 GMT  
		Size: 3.4 MB (3389949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd8dfe81186ff0b816407ebca7cde7473e4568a00053e41a9b865506bb318b0`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334d36e8d2a2055d1ce374a4db658c40f1524af962083d9b5da52852d76a46cd`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0acb58cf5a910482ee59a629e47ddf2882796d6846f7fcba3860c753046c3`  
		Last Modified: Thu, 04 Dec 2025 00:34:29 GMT  
		Size: 17.7 MB (17708720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68ee96465b587d4e1d201671d6f38af93ce12e3e8de1e4318ce20a9a3a22aa5`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:629ac163c9e7113117c78d53db8ab7c25aba4ee3de17c2844199d515d03b1900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63d85a6970c712972dadb4c3f5562f4814c08c63e23177be3b9fb30441e0646`

```dockerfile
```

-	Layers:
	-	`sha256:a9a45b6a9af3185edc3fef012c4ee2bbc1e2310c25a9b46260487d287c102821`  
		Last Modified: Thu, 04 Dec 2025 03:08:01 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-windowsservercore`

```console
$ docker pull docker@sha256:0eb975351ee9df33c41e2946cbd2143ba55fac8ae27c448d9b3fdbd060e969a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:29.1-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:dcd91f0a9029b88613dc48540fe8c128b08bff07dd8b99f4f0242513176f5297
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3290731333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799920065e3e5f973ef96625fe4937bc2563ef5a8e33a59bcf9de238cabe02f5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 23:27:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:45 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:19 GMT
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
	-	`sha256:d7146b17b5860acc8808e415263a03814888a80daaac674aad997e45e4815684`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcde76394ea2b592fadc80c106462452d55b0d2db294199cd06e6368a24364c`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 399.7 KB (399722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620bb71f2687fad09692e4f84af86fcfcccd93276ea8697e98e13c65e534b9c3`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465405d75d81f743b9557eef457a787436466226d68ca5613d82a7c0b02a84d2`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07117c52ec04e5430ba6c16b89755a395af5dc950c1e1965c1522e0b6c7c9369`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 19.5 MB (19450943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3e1dd17fe0599cd773fe8876a3468ed2785a46b58b877ece7fd1b58b174a22`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb064c05a6de4303a29f355e360b69a0b4018d7f54aadc58e85ed89554d726c`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986e5dffed43d7b98b12e2629e4811443a52b3b642ca30a1a9cd58487af9617`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b3176876e2fd382f76e0a0f989cf351e47e43b0507d7e9d91f5846ac99ea9`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 23.9 MB (23949262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591161397992bd49794d31aa33971c487096caccf147b7786c1e0a755a9fe805`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5d7df70beef98e61be396a7a9c43f445629c0394d49ad6b7245913efaf99a2`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e81f136de465956899822ab4c68c183a31a5a4568f59543513268a0cd87b4`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c959e0b45832e9394f8ced26f7a951cfa65a205041622a521e760b10428ac80`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 11.5 MB (11463861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.1-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:e510d0ffbc8c058424c173f9fdc8cf04cc404418596a5affa555804099d86454
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1825263813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f07aa98e515049fbc2b1e495db11a4b0d477c90d0af1e624c7091898258e4fa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Wed, 03 Dec 2025 23:27:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:29 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:28:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:28:55 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:22 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:37 GMT
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
	-	`sha256:f95ab1d322f7331427de0527a98516714be5fdfab8001a0c3afbfdd375f8c704`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997dee9e9b12bed5bc50b78d9d4a23fa986d3c820f38741c6df0273e145b4228`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 501.4 KB (501396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8221a12dd08308b3b8cd4120faa67fcdef9df7d39a4a7acd1474ee4b616290`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88be20e3446295169e1821cf2636d87b5284dd5ea89d65f2b8d6928855ae5b8`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8279728faba290f6ba2b243e3e21a5a11dec89f4ef7ce8e21bc6efb45beb59`  
		Last Modified: Wed, 03 Dec 2025 23:41:22 GMT  
		Size: 19.4 MB (19424449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0ef6633566397de87875a06aae522041d6e3b3a4004ac25a21f129c00b741f`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a349148f8226a779c9bac7fe27b9bb6662d9f5d28cb22d5969722e7e79b280`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4c28f07a327eb3afb667f83caa8e98c39382dcf476cbc17b52e84e0a43092b`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6508f164b53e8ff2ae3c44be363df93cbfcb58724fadaeae0c3dc1170b3acd`  
		Last Modified: Wed, 03 Dec 2025 23:41:23 GMT  
		Size: 23.9 MB (23925342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb3468481b597bde6c2cf074d7b9737c7a77424f16922fbc386ea348e80025`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f80013208797c388923aa4d38cbea4495d3ea0c614ed53a2293f41f22d21a84`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187a71b662b80ffd9fe1339b7e7d5cbff0079de921771aac208a9b839ae48b2`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be497084a394b66ecc710847dddcef4176a5a319c37cb4b40d904e72c8c9a5`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 11.4 MB (11439399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:983813a6983c58f428973a22873ce9e8091209be5490d03e1b2b1a61196967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:29.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:e510d0ffbc8c058424c173f9fdc8cf04cc404418596a5affa555804099d86454
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1825263813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f07aa98e515049fbc2b1e495db11a4b0d477c90d0af1e624c7091898258e4fa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Wed, 03 Dec 2025 23:27:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:29 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:28:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:28:55 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:22 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:37 GMT
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
	-	`sha256:f95ab1d322f7331427de0527a98516714be5fdfab8001a0c3afbfdd375f8c704`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997dee9e9b12bed5bc50b78d9d4a23fa986d3c820f38741c6df0273e145b4228`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 501.4 KB (501396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8221a12dd08308b3b8cd4120faa67fcdef9df7d39a4a7acd1474ee4b616290`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88be20e3446295169e1821cf2636d87b5284dd5ea89d65f2b8d6928855ae5b8`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8279728faba290f6ba2b243e3e21a5a11dec89f4ef7ce8e21bc6efb45beb59`  
		Last Modified: Wed, 03 Dec 2025 23:41:22 GMT  
		Size: 19.4 MB (19424449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0ef6633566397de87875a06aae522041d6e3b3a4004ac25a21f129c00b741f`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a349148f8226a779c9bac7fe27b9bb6662d9f5d28cb22d5969722e7e79b280`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4c28f07a327eb3afb667f83caa8e98c39382dcf476cbc17b52e84e0a43092b`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6508f164b53e8ff2ae3c44be363df93cbfcb58724fadaeae0c3dc1170b3acd`  
		Last Modified: Wed, 03 Dec 2025 23:41:23 GMT  
		Size: 23.9 MB (23925342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb3468481b597bde6c2cf074d7b9737c7a77424f16922fbc386ea348e80025`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f80013208797c388923aa4d38cbea4495d3ea0c614ed53a2293f41f22d21a84`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187a71b662b80ffd9fe1339b7e7d5cbff0079de921771aac208a9b839ae48b2`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be497084a394b66ecc710847dddcef4176a5a319c37cb4b40d904e72c8c9a5`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 11.4 MB (11439399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:2d936418a8c21ad8678fc7b3af4cbb724a2ea1347653cbac3ad6603facd89118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:29.1-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:dcd91f0a9029b88613dc48540fe8c128b08bff07dd8b99f4f0242513176f5297
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3290731333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799920065e3e5f973ef96625fe4937bc2563ef5a8e33a59bcf9de238cabe02f5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 23:27:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:45 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:19 GMT
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
	-	`sha256:d7146b17b5860acc8808e415263a03814888a80daaac674aad997e45e4815684`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcde76394ea2b592fadc80c106462452d55b0d2db294199cd06e6368a24364c`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 399.7 KB (399722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620bb71f2687fad09692e4f84af86fcfcccd93276ea8697e98e13c65e534b9c3`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465405d75d81f743b9557eef457a787436466226d68ca5613d82a7c0b02a84d2`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07117c52ec04e5430ba6c16b89755a395af5dc950c1e1965c1522e0b6c7c9369`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 19.5 MB (19450943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3e1dd17fe0599cd773fe8876a3468ed2785a46b58b877ece7fd1b58b174a22`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb064c05a6de4303a29f355e360b69a0b4018d7f54aadc58e85ed89554d726c`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986e5dffed43d7b98b12e2629e4811443a52b3b642ca30a1a9cd58487af9617`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b3176876e2fd382f76e0a0f989cf351e47e43b0507d7e9d91f5846ac99ea9`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 23.9 MB (23949262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591161397992bd49794d31aa33971c487096caccf147b7786c1e0a755a9fe805`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5d7df70beef98e61be396a7a9c43f445629c0394d49ad6b7245913efaf99a2`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e81f136de465956899822ab4c68c183a31a5a4568f59543513268a0cd87b4`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c959e0b45832e9394f8ced26f7a951cfa65a205041622a521e760b10428ac80`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 11.5 MB (11463861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1.2`

```console
$ docker pull docker@sha256:d47faf85fc5cb4283d7a20c95b6b02d012250b46ec26567554076e2767cb9093
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

### `docker:29.1.2` - linux; amd64

```console
$ docker pull docker@sha256:402b891668de1fe99eb7d054cf25df00a6217232585c02a509ecd7d89ee90856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135884343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b4440e17e983942d30f645a848d94efafacaef8be8733a99feeedc93b05165`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2` - unknown; unknown

```console
$ docker pull docker@sha256:730e45afac3924277c2d3d65bbd80e18019ece14ae5ca8ec59a55372c9357de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4237c7596712be121f7d034be83210391de8307b0ad7f32c6a82e65b63cd5899`

```dockerfile
```

-	Layers:
	-	`sha256:25e1d1a7097f30c7caefc7d07f5efc216727d9595749698f69ba2d3f3c9ac6ce`  
		Last Modified: Thu, 04 Dec 2025 03:07:31 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:fe601bbe28b63642b9b52b7a8478c09ad9007efb3307344dd0200e78ec89757d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128099244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11f21ae0c179baf1e0e49afea4c0c666026627f1546ff28efe88908b2a166f0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:50 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:06 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecc931e2191125378a0a9477c160a961192f08243ea2c2456849e3d27e222e0`  
		Last Modified: Wed, 03 Dec 2025 23:23:08 GMT  
		Size: 8.1 MB (8140516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce9f0fdd9a6972893cb9174962100c606a4ec4f96d43c364367a47626fdf9c`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878cfd957acc34a77a945074318f634f0e69a7c824871f6464251ac78b8a664e`  
		Last Modified: Wed, 03 Dec 2025 23:23:05 GMT  
		Size: 17.6 MB (17560711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff31c3c1cf921e42759f6740e9e0beef431a103e7e0a8d4cc77746069baa2a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57a283bca5c3cafa94cf6aa030b368473a528c61badf87a6acd532479536a3a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 10.2 MB (10195775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d43044fe88440c59cb4d09b26744e4f2a4765098262deecb118d338ea56699`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f15be6ca380c49f5c3b6f9788835a7f811e9ff6921a5c39692cb64255b1572`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2803db336c739715d724a2b06fa65fa1849d95ef8c19e34880c5b5acbc35d88`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f931e0fd6111c2578d5d9a54292a9dfec958fe94d1e7f68f1b31d197a333985`  
		Last Modified: Thu, 04 Dec 2025 00:09:27 GMT  
		Size: 7.2 MB (7230286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc7b8d7478ef5f2f5ba1e5db11c0fc93bd20eafe6b7606d9d47bf2331a2b3c`  
		Last Modified: Thu, 04 Dec 2025 00:09:28 GMT  
		Size: 90.0 KB (89955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d076abb53c41564afd763287157cf740f81e0db1053596ab43b14cd7ef71b07d`  
		Last Modified: Thu, 04 Dec 2025 00:09:25 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a101330bea32635e63394dee524dbef13c06b88980cbb82594b56006da57986`  
		Last Modified: Thu, 04 Dec 2025 00:09:31 GMT  
		Size: 59.9 MB (59893215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc26c05faa4dc67c6281383dfb1b858e05d90847279c446859a199658f586ac2`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdb33cb903b3e7bbad1c970a6cad894a4a031db43544a2245b7413b8146a78f`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2` - unknown; unknown

```console
$ docker pull docker@sha256:d42c8cf8a28b5613be8a5e682d1f0adc2a66593fc5825c921cbeb79908537a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c000f8f0e671395bd4558756b0240d013b2b9f86f582f6aebdb340e1c0bde`

```dockerfile
```

-	Layers:
	-	`sha256:c8b0bc7a5fcd7022ef2328012ba0f8cd8d24946692ba523f6780c59afcf2c0c5`  
		Last Modified: Thu, 04 Dec 2025 03:07:33 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:3b20b2f3273127bc77b0d5a10d6c89fbe489c6e26aabfcf70374718b183dfaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126234834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30509973b0ac1a4da60db5cd58eafc1683ae159d63618ea8b33fac2fea969ec9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:31 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:32 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935a3faa05b5054eb2d5539416291930c560ec5c5562fc406afa35bd473fb0e6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 7.5 MB (7461370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde152eb030abb1c199a35f2e9e0e6b1b6a57d4feb903df63b11037fac1a2ce6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f06bd5e7fd9b6ded91c70f08fd128821578ffc9820598e8f07b40cfb0d9ce5`  
		Last Modified: Wed, 03 Dec 2025 23:23:55 GMT  
		Size: 17.6 MB (17550088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afc00eecc90cef8da7558059bc5d03c4e8a6fcc711de9e737079165e731684`  
		Last Modified: Wed, 03 Dec 2025 23:23:50 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515c94502ad1a992ad7e0b00b558d157c6f159b4e9db4d9d2f40e7bafb17b92e`  
		Last Modified: Wed, 03 Dec 2025 23:23:52 GMT  
		Size: 10.2 MB (10188522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bee705c92c06181488e34193ffad6a12b619e780a07b1a79299bf5f0145f4d`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a23011c0e0e10c3d92ecd1d44a351ea1c7caa7b8dd85a808ee2e3d7b21fb6f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa197bf85b5aea7f0c51679266daa38199c6e7991b49320c5c16206a14c279f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3c3136863c024060420d7807c203025bc548ac5ad2b0858e446809ab410c`  
		Last Modified: Thu, 04 Dec 2025 00:09:54 GMT  
		Size: 6.5 MB (6538168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f77e8b986e32956581155ff6b177404ce1edb49d73437dd38ef58279f920ef`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 86.4 KB (86396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348c52291ee0284e8483fdfff7481d25d34bb401399ce821ec03bcb55d4d2e94`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018fd645a77660c02db5a21d598961bc1ed40e8aa011a2c6590fef87930aa5e`  
		Last Modified: Thu, 04 Dec 2025 00:09:57 GMT  
		Size: 59.7 MB (59725684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daf7cac083af2912d7cad82e45f8086baaba542e7e0aa6d43a21ce73dff00c`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88842983720a1ed7d8aa571666aff44394345c26366bf0d54590b6ff3eda3a84`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2` - unknown; unknown

```console
$ docker pull docker@sha256:9960273ea153bbe574b692c69e822b3013ee15f4c6c70e6a909ca44ec1ab3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1927298a387e339d847056a865f7134a8cfc0b73ce2d584fdaf95fa1bc81a8`

```dockerfile
```

-	Layers:
	-	`sha256:6007395b9d82e0ffe5855b313e61375469e3ae796653dc07903f13486fc11870`  
		Last Modified: Thu, 04 Dec 2025 03:07:36 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7c26d2db80935c936465085344b49347e1a3d64aab63c61dde7cb47fb85b0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125991288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb84df0944fb8b77d9caae220f0fe4e6533a8b0bb7ac9d1fe0ab537611d7539`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2` - unknown; unknown

```console
$ docker pull docker@sha256:fff37f801a284572fb4ec647febb83d21fa848330ad16164593fd754054e4e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eda8b90f0af1ce070ab1b486d36a6f8e52a00099f86dff74b9ede6cbeb4d19c`

```dockerfile
```

-	Layers:
	-	`sha256:7f49d359152acc433dd0182ab053b3a9885e5cbd5434e49990d59ff25fc3a484`  
		Last Modified: Thu, 04 Dec 2025 03:07:40 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.2-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.1.2-cli`

```console
$ docker pull docker@sha256:d525718bb067b852a3a33c49485e5f5ac412be1e6e76f7551bdc202d5a889f85
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

### `docker:29.1.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:21a1c55469066f188822c840c6524d53ee9839e22016d44ef7fbe33a9cd86d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64714559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19f3c0eff8641da7c2b0ce16d81b1d40c260a23d505336cbec71a4efd465fe7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a151e1882a0ff66dc0af0fe6d18ca20c53f882957b702f02182f533230db9086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239e883311e13240a894908074353c98ca40cc658715597bddde6eab0d29f26`

```dockerfile
```

-	Layers:
	-	`sha256:216ce815280ec2d0835d77acdeab97fbee9288506643bbc7cb64e692fda85d7a`  
		Last Modified: Thu, 04 Dec 2025 03:07:45 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d0265fe0ee552de65a6516d3f06ae73a1653bceec355a4aefe8e354b39c76331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61104123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39a447a955d8f055f4d11bdbd35660231a7f8d130c8074aa02e142c343a3208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:18:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:18:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:18:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:18:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:18:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:18:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:18:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6abcf03c4d2a46ff1f3cf4e321bc7993d4d20b17f12f99d466b39b3555298`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 8.3 MB (8301067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb792a943c4d38855261216162c97e27587aa936e4de5451eeda4d170348a07`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aa1d961beedab5a903eed7b199a7f3cf448a9ad0d235f989735bce0000963`  
		Last Modified: Thu, 04 Dec 2025 01:19:02 GMT  
		Size: 17.6 MB (17560675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136294917ec3532038026ad3f18199c6aff9e645109302b3c9fdc832bf5dd82`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 21.5 MB (21476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0b74dd96a21e6b38324422ba118ccd940a01d181d09275193f948ebd543d2`  
		Last Modified: Thu, 04 Dec 2025 01:19:00 GMT  
		Size: 10.2 MB (10195783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a193c8f7c9fb004babea7c82efc513b5196991d924daf956f6881012fec3`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86d05610e4cf2f79db6d09c9b4c2c8944991a0da701d442726824c5daf33ae`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ebf88cb27a0d9b7e72386749701cbb0df6c753c53caa647578e1151c9f6e0`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc76e87252fb09b02cea86a5b617829392911cde87352fad99dd8bfac4f35cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24448a333caa52a4c783c364a476d2027af604ef74cec044324f6a28724416c5`

```dockerfile
```

-	Layers:
	-	`sha256:4c5c12bece34bf0cfd9182ec595bd154f82fce5392e2d8805658d591a8ddbffe`  
		Last Modified: Thu, 04 Dec 2025 03:07:48 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:935d68f5bf42e536d86f411c2b8a9cedb7cadd4b2e5c4901ed9c19b4f5843297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60072150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ecb3dd3fccd1770e4077f98543a49bb4b3b56dc6c3aa9c2079622abb19001`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:17:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:17:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:17:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:17:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:17:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:17:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:17:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:17:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:17:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab67aee2b47b20a25046ed73de706bd5a80ad82192c27db420a65cfa5fb17cb`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 7.6 MB (7598018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860397c02592909361c994060954f1d684dc0366a2df922a3fe521f02a6b6b2`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ddf54b4c1a081004e3eb1cd154ca1c1cc7e169e416c1ebb9fb23b872919a4d`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 17.6 MB (17550083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645b95707890af1cad5443377a3d8bba32e3701d1f59ee629bd3a1598e45b63`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 21.5 MB (21454910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d968e842fbfa0f7d8d14048d776e945449a586f5772cf04dc12753e58629d9`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 10.2 MB (10188525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482495d52b3d32ead0b4c76816259e750cf45944ac6a48937ed5de349bc73b`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862303f1e616b7c4e5debf343f489e54323b1d7e8d897d6bbcf9951c6fb125e7`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b42590dfec33aa271798a0fdbb5fb080fa6137a58beb89183e43d609cc24`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f53d3adf38731e16863cf838919c725a7485c9343ed47dbe1819cb1eee9fcf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc530b6722d835f222fc005e4ecfc18f010f44d9177c01b8d3fb440e2270eb41`

```dockerfile
```

-	Layers:
	-	`sha256:250e1a2b917f39d22919fc8dfe5a354dcb0d945d2986b1d8ee076e7360e0d189`  
		Last Modified: Thu, 04 Dec 2025 03:07:52 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:05be5900b65fb6922962f3a5cd458bfa73a54fc06caa4147088d27fbcbfbd629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60569466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f578b3c9f73f992024507d6c2ca3b91941f9e7640a6f4d0c06e3abf802ecfcfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:53b87f74f0453103d0e91fd60ae5257848aaf5b69a305e7473eea62bf9dd55b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f007f56500be77ded77125653b2b2062bcf4f13495e20a149611f5435b4cf1e6`

```dockerfile
```

-	Layers:
	-	`sha256:64d865b942bb61e404183343df3b7b76011d6dc7ce17dbb5ea00e4380a7e0293`  
		Last Modified: Thu, 04 Dec 2025 03:07:55 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.2-cli-alpine3.23`

```console
$ docker pull docker@sha256:d525718bb067b852a3a33c49485e5f5ac412be1e6e76f7551bdc202d5a889f85
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

### `docker:29.1.2-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:21a1c55469066f188822c840c6524d53ee9839e22016d44ef7fbe33a9cd86d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64714559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19f3c0eff8641da7c2b0ce16d81b1d40c260a23d505336cbec71a4efd465fe7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:a151e1882a0ff66dc0af0fe6d18ca20c53f882957b702f02182f533230db9086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239e883311e13240a894908074353c98ca40cc658715597bddde6eab0d29f26`

```dockerfile
```

-	Layers:
	-	`sha256:216ce815280ec2d0835d77acdeab97fbee9288506643bbc7cb64e692fda85d7a`  
		Last Modified: Thu, 04 Dec 2025 03:07:45 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:d0265fe0ee552de65a6516d3f06ae73a1653bceec355a4aefe8e354b39c76331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61104123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39a447a955d8f055f4d11bdbd35660231a7f8d130c8074aa02e142c343a3208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:18:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:18:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:18:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:18:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:18:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:18:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:18:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6abcf03c4d2a46ff1f3cf4e321bc7993d4d20b17f12f99d466b39b3555298`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 8.3 MB (8301067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb792a943c4d38855261216162c97e27587aa936e4de5451eeda4d170348a07`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aa1d961beedab5a903eed7b199a7f3cf448a9ad0d235f989735bce0000963`  
		Last Modified: Thu, 04 Dec 2025 01:19:02 GMT  
		Size: 17.6 MB (17560675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136294917ec3532038026ad3f18199c6aff9e645109302b3c9fdc832bf5dd82`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 21.5 MB (21476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0b74dd96a21e6b38324422ba118ccd940a01d181d09275193f948ebd543d2`  
		Last Modified: Thu, 04 Dec 2025 01:19:00 GMT  
		Size: 10.2 MB (10195783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a193c8f7c9fb004babea7c82efc513b5196991d924daf956f6881012fec3`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86d05610e4cf2f79db6d09c9b4c2c8944991a0da701d442726824c5daf33ae`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ebf88cb27a0d9b7e72386749701cbb0df6c753c53caa647578e1151c9f6e0`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:dc76e87252fb09b02cea86a5b617829392911cde87352fad99dd8bfac4f35cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24448a333caa52a4c783c364a476d2027af604ef74cec044324f6a28724416c5`

```dockerfile
```

-	Layers:
	-	`sha256:4c5c12bece34bf0cfd9182ec595bd154f82fce5392e2d8805658d591a8ddbffe`  
		Last Modified: Thu, 04 Dec 2025 03:07:48 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:935d68f5bf42e536d86f411c2b8a9cedb7cadd4b2e5c4901ed9c19b4f5843297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60072150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ecb3dd3fccd1770e4077f98543a49bb4b3b56dc6c3aa9c2079622abb19001`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:17:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:17:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:17:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:17:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:17:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:17:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:17:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:17:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:17:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab67aee2b47b20a25046ed73de706bd5a80ad82192c27db420a65cfa5fb17cb`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 7.6 MB (7598018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860397c02592909361c994060954f1d684dc0366a2df922a3fe521f02a6b6b2`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ddf54b4c1a081004e3eb1cd154ca1c1cc7e169e416c1ebb9fb23b872919a4d`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 17.6 MB (17550083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645b95707890af1cad5443377a3d8bba32e3701d1f59ee629bd3a1598e45b63`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 21.5 MB (21454910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d968e842fbfa0f7d8d14048d776e945449a586f5772cf04dc12753e58629d9`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 10.2 MB (10188525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482495d52b3d32ead0b4c76816259e750cf45944ac6a48937ed5de349bc73b`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862303f1e616b7c4e5debf343f489e54323b1d7e8d897d6bbcf9951c6fb125e7`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b42590dfec33aa271798a0fdbb5fb080fa6137a58beb89183e43d609cc24`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:f53d3adf38731e16863cf838919c725a7485c9343ed47dbe1819cb1eee9fcf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc530b6722d835f222fc005e4ecfc18f010f44d9177c01b8d3fb440e2270eb41`

```dockerfile
```

-	Layers:
	-	`sha256:250e1a2b917f39d22919fc8dfe5a354dcb0d945d2986b1d8ee076e7360e0d189`  
		Last Modified: Thu, 04 Dec 2025 03:07:52 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:05be5900b65fb6922962f3a5cd458bfa73a54fc06caa4147088d27fbcbfbd629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60569466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f578b3c9f73f992024507d6c2ca3b91941f9e7640a6f4d0c06e3abf802ecfcfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:53b87f74f0453103d0e91fd60ae5257848aaf5b69a305e7473eea62bf9dd55b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f007f56500be77ded77125653b2b2062bcf4f13495e20a149611f5435b4cf1e6`

```dockerfile
```

-	Layers:
	-	`sha256:64d865b942bb61e404183343df3b7b76011d6dc7ce17dbb5ea00e4380a7e0293`  
		Last Modified: Thu, 04 Dec 2025 03:07:55 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.2-dind`

```console
$ docker pull docker@sha256:d47faf85fc5cb4283d7a20c95b6b02d012250b46ec26567554076e2767cb9093
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

### `docker:29.1.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:402b891668de1fe99eb7d054cf25df00a6217232585c02a509ecd7d89ee90856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135884343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b4440e17e983942d30f645a848d94efafacaef8be8733a99feeedc93b05165`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:730e45afac3924277c2d3d65bbd80e18019ece14ae5ca8ec59a55372c9357de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4237c7596712be121f7d034be83210391de8307b0ad7f32c6a82e65b63cd5899`

```dockerfile
```

-	Layers:
	-	`sha256:25e1d1a7097f30c7caefc7d07f5efc216727d9595749698f69ba2d3f3c9ac6ce`  
		Last Modified: Thu, 04 Dec 2025 03:07:31 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:fe601bbe28b63642b9b52b7a8478c09ad9007efb3307344dd0200e78ec89757d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128099244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11f21ae0c179baf1e0e49afea4c0c666026627f1546ff28efe88908b2a166f0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:50 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:06 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecc931e2191125378a0a9477c160a961192f08243ea2c2456849e3d27e222e0`  
		Last Modified: Wed, 03 Dec 2025 23:23:08 GMT  
		Size: 8.1 MB (8140516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce9f0fdd9a6972893cb9174962100c606a4ec4f96d43c364367a47626fdf9c`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878cfd957acc34a77a945074318f634f0e69a7c824871f6464251ac78b8a664e`  
		Last Modified: Wed, 03 Dec 2025 23:23:05 GMT  
		Size: 17.6 MB (17560711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff31c3c1cf921e42759f6740e9e0beef431a103e7e0a8d4cc77746069baa2a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57a283bca5c3cafa94cf6aa030b368473a528c61badf87a6acd532479536a3a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 10.2 MB (10195775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d43044fe88440c59cb4d09b26744e4f2a4765098262deecb118d338ea56699`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f15be6ca380c49f5c3b6f9788835a7f811e9ff6921a5c39692cb64255b1572`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2803db336c739715d724a2b06fa65fa1849d95ef8c19e34880c5b5acbc35d88`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f931e0fd6111c2578d5d9a54292a9dfec958fe94d1e7f68f1b31d197a333985`  
		Last Modified: Thu, 04 Dec 2025 00:09:27 GMT  
		Size: 7.2 MB (7230286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc7b8d7478ef5f2f5ba1e5db11c0fc93bd20eafe6b7606d9d47bf2331a2b3c`  
		Last Modified: Thu, 04 Dec 2025 00:09:28 GMT  
		Size: 90.0 KB (89955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d076abb53c41564afd763287157cf740f81e0db1053596ab43b14cd7ef71b07d`  
		Last Modified: Thu, 04 Dec 2025 00:09:25 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a101330bea32635e63394dee524dbef13c06b88980cbb82594b56006da57986`  
		Last Modified: Thu, 04 Dec 2025 00:09:31 GMT  
		Size: 59.9 MB (59893215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc26c05faa4dc67c6281383dfb1b858e05d90847279c446859a199658f586ac2`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdb33cb903b3e7bbad1c970a6cad894a4a031db43544a2245b7413b8146a78f`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d42c8cf8a28b5613be8a5e682d1f0adc2a66593fc5825c921cbeb79908537a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c000f8f0e671395bd4558756b0240d013b2b9f86f582f6aebdb340e1c0bde`

```dockerfile
```

-	Layers:
	-	`sha256:c8b0bc7a5fcd7022ef2328012ba0f8cd8d24946692ba523f6780c59afcf2c0c5`  
		Last Modified: Thu, 04 Dec 2025 03:07:33 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:3b20b2f3273127bc77b0d5a10d6c89fbe489c6e26aabfcf70374718b183dfaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126234834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30509973b0ac1a4da60db5cd58eafc1683ae159d63618ea8b33fac2fea969ec9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:31 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:32 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935a3faa05b5054eb2d5539416291930c560ec5c5562fc406afa35bd473fb0e6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 7.5 MB (7461370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde152eb030abb1c199a35f2e9e0e6b1b6a57d4feb903df63b11037fac1a2ce6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f06bd5e7fd9b6ded91c70f08fd128821578ffc9820598e8f07b40cfb0d9ce5`  
		Last Modified: Wed, 03 Dec 2025 23:23:55 GMT  
		Size: 17.6 MB (17550088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afc00eecc90cef8da7558059bc5d03c4e8a6fcc711de9e737079165e731684`  
		Last Modified: Wed, 03 Dec 2025 23:23:50 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515c94502ad1a992ad7e0b00b558d157c6f159b4e9db4d9d2f40e7bafb17b92e`  
		Last Modified: Wed, 03 Dec 2025 23:23:52 GMT  
		Size: 10.2 MB (10188522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bee705c92c06181488e34193ffad6a12b619e780a07b1a79299bf5f0145f4d`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a23011c0e0e10c3d92ecd1d44a351ea1c7caa7b8dd85a808ee2e3d7b21fb6f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa197bf85b5aea7f0c51679266daa38199c6e7991b49320c5c16206a14c279f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3c3136863c024060420d7807c203025bc548ac5ad2b0858e446809ab410c`  
		Last Modified: Thu, 04 Dec 2025 00:09:54 GMT  
		Size: 6.5 MB (6538168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f77e8b986e32956581155ff6b177404ce1edb49d73437dd38ef58279f920ef`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 86.4 KB (86396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348c52291ee0284e8483fdfff7481d25d34bb401399ce821ec03bcb55d4d2e94`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018fd645a77660c02db5a21d598961bc1ed40e8aa011a2c6590fef87930aa5e`  
		Last Modified: Thu, 04 Dec 2025 00:09:57 GMT  
		Size: 59.7 MB (59725684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daf7cac083af2912d7cad82e45f8086baaba542e7e0aa6d43a21ce73dff00c`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88842983720a1ed7d8aa571666aff44394345c26366bf0d54590b6ff3eda3a84`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9960273ea153bbe574b692c69e822b3013ee15f4c6c70e6a909ca44ec1ab3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1927298a387e339d847056a865f7134a8cfc0b73ce2d584fdaf95fa1bc81a8`

```dockerfile
```

-	Layers:
	-	`sha256:6007395b9d82e0ffe5855b313e61375469e3ae796653dc07903f13486fc11870`  
		Last Modified: Thu, 04 Dec 2025 03:07:36 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7c26d2db80935c936465085344b49347e1a3d64aab63c61dde7cb47fb85b0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125991288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb84df0944fb8b77d9caae220f0fe4e6533a8b0bb7ac9d1fe0ab537611d7539`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fff37f801a284572fb4ec647febb83d21fa848330ad16164593fd754054e4e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eda8b90f0af1ce070ab1b486d36a6f8e52a00099f86dff74b9ede6cbeb4d19c`

```dockerfile
```

-	Layers:
	-	`sha256:7f49d359152acc433dd0182ab053b3a9885e5cbd5434e49990d59ff25fc3a484`  
		Last Modified: Thu, 04 Dec 2025 03:07:40 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.2-dind-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.1.2-dind-rootless`

```console
$ docker pull docker@sha256:421dffbe324135321070051128d9d2787f0465a94d728070953b89255438a5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.1.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:353a1727d0e6ac8343824427ff6d442390472e0bb77ca01655da0ddcf51fb9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156655034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfdf4d733c409824955ff98bc575e0384deb01f66c4f8e9a244e158f749ea1f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
# Thu, 04 Dec 2025 00:34:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 00:34:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 00:34:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 00:34:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91aa056e56aa4a66ab4445fc928d9900f02526039d0d9e034dbd5f1864ded0e`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 3.4 MB (3398378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ba6b907925696d4f4bf8e90017155cfc57c2eb3a3daf7b148f8e03ec3e6e46`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa8d4bd6998c2fe7060be7b4c380915afb0718f2a048cffec66cfa2b3396679`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb4f0a9a116b4469861628ca4fa5396cf4046b9589a4d19291e11bfea5fc4c6`  
		Last Modified: Thu, 04 Dec 2025 00:34:49 GMT  
		Size: 17.4 MB (17370975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0121931059414c5b535a820a06149e50072743b8d7d9d1292e94b5dd7cde587f`  
		Last Modified: Thu, 04 Dec 2025 00:34:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4b08832b0e539cc368981d37d867659cadd73c07d5b17094e24239509d6d408f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2014725d32624c20c843af1525ac27aa85a87442225e3a832e40bb9658fa40`

```dockerfile
```

-	Layers:
	-	`sha256:d430a287400d6e64aca730c1235ea91292ca5733da9bb24288faf42078d9d405`  
		Last Modified: Thu, 04 Dec 2025 03:07:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a1db98f222784429b330f778f1957ad3018c290fa95637335ca9ee58c09bd1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147091297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c01b600ca0f7971b32388b10745a1245988aa3e8ca83212a3ea4c2b2eb9609c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
# Thu, 04 Dec 2025 00:34:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 00:34:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 00:34:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 00:34:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29744f0d4e84a604abd643d72e500a942b93b47aebc9608aeb11c9547505978f`  
		Last Modified: Thu, 04 Dec 2025 00:34:30 GMT  
		Size: 3.4 MB (3389949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd8dfe81186ff0b816407ebca7cde7473e4568a00053e41a9b865506bb318b0`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334d36e8d2a2055d1ce374a4db658c40f1524af962083d9b5da52852d76a46cd`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0acb58cf5a910482ee59a629e47ddf2882796d6846f7fcba3860c753046c3`  
		Last Modified: Thu, 04 Dec 2025 00:34:29 GMT  
		Size: 17.7 MB (17708720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68ee96465b587d4e1d201671d6f38af93ce12e3e8de1e4318ce20a9a3a22aa5`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:629ac163c9e7113117c78d53db8ab7c25aba4ee3de17c2844199d515d03b1900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63d85a6970c712972dadb4c3f5562f4814c08c63e23177be3b9fb30441e0646`

```dockerfile
```

-	Layers:
	-	`sha256:a9a45b6a9af3185edc3fef012c4ee2bbc1e2310c25a9b46260487d287c102821`  
		Last Modified: Thu, 04 Dec 2025 03:08:01 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.2-windowsservercore`

```console
$ docker pull docker@sha256:0eb975351ee9df33c41e2946cbd2143ba55fac8ae27c448d9b3fdbd060e969a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:29.1.2-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:dcd91f0a9029b88613dc48540fe8c128b08bff07dd8b99f4f0242513176f5297
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3290731333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799920065e3e5f973ef96625fe4937bc2563ef5a8e33a59bcf9de238cabe02f5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 23:27:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:45 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:19 GMT
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
	-	`sha256:d7146b17b5860acc8808e415263a03814888a80daaac674aad997e45e4815684`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcde76394ea2b592fadc80c106462452d55b0d2db294199cd06e6368a24364c`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 399.7 KB (399722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620bb71f2687fad09692e4f84af86fcfcccd93276ea8697e98e13c65e534b9c3`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465405d75d81f743b9557eef457a787436466226d68ca5613d82a7c0b02a84d2`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07117c52ec04e5430ba6c16b89755a395af5dc950c1e1965c1522e0b6c7c9369`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 19.5 MB (19450943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3e1dd17fe0599cd773fe8876a3468ed2785a46b58b877ece7fd1b58b174a22`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb064c05a6de4303a29f355e360b69a0b4018d7f54aadc58e85ed89554d726c`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986e5dffed43d7b98b12e2629e4811443a52b3b642ca30a1a9cd58487af9617`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b3176876e2fd382f76e0a0f989cf351e47e43b0507d7e9d91f5846ac99ea9`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 23.9 MB (23949262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591161397992bd49794d31aa33971c487096caccf147b7786c1e0a755a9fe805`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5d7df70beef98e61be396a7a9c43f445629c0394d49ad6b7245913efaf99a2`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e81f136de465956899822ab4c68c183a31a5a4568f59543513268a0cd87b4`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c959e0b45832e9394f8ced26f7a951cfa65a205041622a521e760b10428ac80`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 11.5 MB (11463861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.1.2-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:e510d0ffbc8c058424c173f9fdc8cf04cc404418596a5affa555804099d86454
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1825263813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f07aa98e515049fbc2b1e495db11a4b0d477c90d0af1e624c7091898258e4fa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Wed, 03 Dec 2025 23:27:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:29 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:28:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:28:55 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:22 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:37 GMT
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
	-	`sha256:f95ab1d322f7331427de0527a98516714be5fdfab8001a0c3afbfdd375f8c704`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997dee9e9b12bed5bc50b78d9d4a23fa986d3c820f38741c6df0273e145b4228`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 501.4 KB (501396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8221a12dd08308b3b8cd4120faa67fcdef9df7d39a4a7acd1474ee4b616290`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88be20e3446295169e1821cf2636d87b5284dd5ea89d65f2b8d6928855ae5b8`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8279728faba290f6ba2b243e3e21a5a11dec89f4ef7ce8e21bc6efb45beb59`  
		Last Modified: Wed, 03 Dec 2025 23:41:22 GMT  
		Size: 19.4 MB (19424449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0ef6633566397de87875a06aae522041d6e3b3a4004ac25a21f129c00b741f`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a349148f8226a779c9bac7fe27b9bb6662d9f5d28cb22d5969722e7e79b280`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4c28f07a327eb3afb667f83caa8e98c39382dcf476cbc17b52e84e0a43092b`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6508f164b53e8ff2ae3c44be363df93cbfcb58724fadaeae0c3dc1170b3acd`  
		Last Modified: Wed, 03 Dec 2025 23:41:23 GMT  
		Size: 23.9 MB (23925342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb3468481b597bde6c2cf074d7b9737c7a77424f16922fbc386ea348e80025`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f80013208797c388923aa4d38cbea4495d3ea0c614ed53a2293f41f22d21a84`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187a71b662b80ffd9fe1339b7e7d5cbff0079de921771aac208a9b839ae48b2`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be497084a394b66ecc710847dddcef4176a5a319c37cb4b40d904e72c8c9a5`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 11.4 MB (11439399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:983813a6983c58f428973a22873ce9e8091209be5490d03e1b2b1a61196967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:29.1.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:e510d0ffbc8c058424c173f9fdc8cf04cc404418596a5affa555804099d86454
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1825263813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f07aa98e515049fbc2b1e495db11a4b0d477c90d0af1e624c7091898258e4fa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Wed, 03 Dec 2025 23:27:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:29 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:28:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:28:55 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:22 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:37 GMT
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
	-	`sha256:f95ab1d322f7331427de0527a98516714be5fdfab8001a0c3afbfdd375f8c704`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997dee9e9b12bed5bc50b78d9d4a23fa986d3c820f38741c6df0273e145b4228`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 501.4 KB (501396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8221a12dd08308b3b8cd4120faa67fcdef9df7d39a4a7acd1474ee4b616290`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88be20e3446295169e1821cf2636d87b5284dd5ea89d65f2b8d6928855ae5b8`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8279728faba290f6ba2b243e3e21a5a11dec89f4ef7ce8e21bc6efb45beb59`  
		Last Modified: Wed, 03 Dec 2025 23:41:22 GMT  
		Size: 19.4 MB (19424449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0ef6633566397de87875a06aae522041d6e3b3a4004ac25a21f129c00b741f`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a349148f8226a779c9bac7fe27b9bb6662d9f5d28cb22d5969722e7e79b280`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4c28f07a327eb3afb667f83caa8e98c39382dcf476cbc17b52e84e0a43092b`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6508f164b53e8ff2ae3c44be363df93cbfcb58724fadaeae0c3dc1170b3acd`  
		Last Modified: Wed, 03 Dec 2025 23:41:23 GMT  
		Size: 23.9 MB (23925342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb3468481b597bde6c2cf074d7b9737c7a77424f16922fbc386ea348e80025`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f80013208797c388923aa4d38cbea4495d3ea0c614ed53a2293f41f22d21a84`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187a71b662b80ffd9fe1339b7e7d5cbff0079de921771aac208a9b839ae48b2`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be497084a394b66ecc710847dddcef4176a5a319c37cb4b40d904e72c8c9a5`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 11.4 MB (11439399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:2d936418a8c21ad8678fc7b3af4cbb724a2ea1347653cbac3ad6603facd89118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:29.1.2-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:dcd91f0a9029b88613dc48540fe8c128b08bff07dd8b99f4f0242513176f5297
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3290731333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799920065e3e5f973ef96625fe4937bc2563ef5a8e33a59bcf9de238cabe02f5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 23:27:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:45 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:19 GMT
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
	-	`sha256:d7146b17b5860acc8808e415263a03814888a80daaac674aad997e45e4815684`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcde76394ea2b592fadc80c106462452d55b0d2db294199cd06e6368a24364c`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 399.7 KB (399722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620bb71f2687fad09692e4f84af86fcfcccd93276ea8697e98e13c65e534b9c3`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465405d75d81f743b9557eef457a787436466226d68ca5613d82a7c0b02a84d2`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07117c52ec04e5430ba6c16b89755a395af5dc950c1e1965c1522e0b6c7c9369`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 19.5 MB (19450943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3e1dd17fe0599cd773fe8876a3468ed2785a46b58b877ece7fd1b58b174a22`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb064c05a6de4303a29f355e360b69a0b4018d7f54aadc58e85ed89554d726c`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986e5dffed43d7b98b12e2629e4811443a52b3b642ca30a1a9cd58487af9617`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b3176876e2fd382f76e0a0f989cf351e47e43b0507d7e9d91f5846ac99ea9`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 23.9 MB (23949262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591161397992bd49794d31aa33971c487096caccf147b7786c1e0a755a9fe805`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5d7df70beef98e61be396a7a9c43f445629c0394d49ad6b7245913efaf99a2`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e81f136de465956899822ab4c68c183a31a5a4568f59543513268a0cd87b4`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c959e0b45832e9394f8ced26f7a951cfa65a205041622a521e760b10428ac80`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 11.5 MB (11463861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:d525718bb067b852a3a33c49485e5f5ac412be1e6e76f7551bdc202d5a889f85
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
$ docker pull docker@sha256:21a1c55469066f188822c840c6524d53ee9839e22016d44ef7fbe33a9cd86d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64714559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19f3c0eff8641da7c2b0ce16d81b1d40c260a23d505336cbec71a4efd465fe7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a151e1882a0ff66dc0af0fe6d18ca20c53f882957b702f02182f533230db9086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239e883311e13240a894908074353c98ca40cc658715597bddde6eab0d29f26`

```dockerfile
```

-	Layers:
	-	`sha256:216ce815280ec2d0835d77acdeab97fbee9288506643bbc7cb64e692fda85d7a`  
		Last Modified: Thu, 04 Dec 2025 03:07:45 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d0265fe0ee552de65a6516d3f06ae73a1653bceec355a4aefe8e354b39c76331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61104123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39a447a955d8f055f4d11bdbd35660231a7f8d130c8074aa02e142c343a3208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:18:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:18:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:18:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:18:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:18:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:18:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:18:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6abcf03c4d2a46ff1f3cf4e321bc7993d4d20b17f12f99d466b39b3555298`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 8.3 MB (8301067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb792a943c4d38855261216162c97e27587aa936e4de5451eeda4d170348a07`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aa1d961beedab5a903eed7b199a7f3cf448a9ad0d235f989735bce0000963`  
		Last Modified: Thu, 04 Dec 2025 01:19:02 GMT  
		Size: 17.6 MB (17560675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136294917ec3532038026ad3f18199c6aff9e645109302b3c9fdc832bf5dd82`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 21.5 MB (21476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0b74dd96a21e6b38324422ba118ccd940a01d181d09275193f948ebd543d2`  
		Last Modified: Thu, 04 Dec 2025 01:19:00 GMT  
		Size: 10.2 MB (10195783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a193c8f7c9fb004babea7c82efc513b5196991d924daf956f6881012fec3`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86d05610e4cf2f79db6d09c9b4c2c8944991a0da701d442726824c5daf33ae`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ebf88cb27a0d9b7e72386749701cbb0df6c753c53caa647578e1151c9f6e0`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc76e87252fb09b02cea86a5b617829392911cde87352fad99dd8bfac4f35cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24448a333caa52a4c783c364a476d2027af604ef74cec044324f6a28724416c5`

```dockerfile
```

-	Layers:
	-	`sha256:4c5c12bece34bf0cfd9182ec595bd154f82fce5392e2d8805658d591a8ddbffe`  
		Last Modified: Thu, 04 Dec 2025 03:07:48 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:935d68f5bf42e536d86f411c2b8a9cedb7cadd4b2e5c4901ed9c19b4f5843297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60072150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ecb3dd3fccd1770e4077f98543a49bb4b3b56dc6c3aa9c2079622abb19001`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:17:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:17:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:17:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:17:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:17:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:17:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:17:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:17:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:17:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab67aee2b47b20a25046ed73de706bd5a80ad82192c27db420a65cfa5fb17cb`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 7.6 MB (7598018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860397c02592909361c994060954f1d684dc0366a2df922a3fe521f02a6b6b2`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ddf54b4c1a081004e3eb1cd154ca1c1cc7e169e416c1ebb9fb23b872919a4d`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 17.6 MB (17550083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645b95707890af1cad5443377a3d8bba32e3701d1f59ee629bd3a1598e45b63`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 21.5 MB (21454910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d968e842fbfa0f7d8d14048d776e945449a586f5772cf04dc12753e58629d9`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 10.2 MB (10188525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482495d52b3d32ead0b4c76816259e750cf45944ac6a48937ed5de349bc73b`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862303f1e616b7c4e5debf343f489e54323b1d7e8d897d6bbcf9951c6fb125e7`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b42590dfec33aa271798a0fdbb5fb080fa6137a58beb89183e43d609cc24`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f53d3adf38731e16863cf838919c725a7485c9343ed47dbe1819cb1eee9fcf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc530b6722d835f222fc005e4ecfc18f010f44d9177c01b8d3fb440e2270eb41`

```dockerfile
```

-	Layers:
	-	`sha256:250e1a2b917f39d22919fc8dfe5a354dcb0d945d2986b1d8ee076e7360e0d189`  
		Last Modified: Thu, 04 Dec 2025 03:07:52 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:05be5900b65fb6922962f3a5cd458bfa73a54fc06caa4147088d27fbcbfbd629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60569466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f578b3c9f73f992024507d6c2ca3b91941f9e7640a6f4d0c06e3abf802ecfcfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:53b87f74f0453103d0e91fd60ae5257848aaf5b69a305e7473eea62bf9dd55b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f007f56500be77ded77125653b2b2062bcf4f13495e20a149611f5435b4cf1e6`

```dockerfile
```

-	Layers:
	-	`sha256:64d865b942bb61e404183343df3b7b76011d6dc7ce17dbb5ea00e4380a7e0293`  
		Last Modified: Thu, 04 Dec 2025 03:07:55 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:d47faf85fc5cb4283d7a20c95b6b02d012250b46ec26567554076e2767cb9093
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
$ docker pull docker@sha256:402b891668de1fe99eb7d054cf25df00a6217232585c02a509ecd7d89ee90856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135884343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b4440e17e983942d30f645a848d94efafacaef8be8733a99feeedc93b05165`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:730e45afac3924277c2d3d65bbd80e18019ece14ae5ca8ec59a55372c9357de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4237c7596712be121f7d034be83210391de8307b0ad7f32c6a82e65b63cd5899`

```dockerfile
```

-	Layers:
	-	`sha256:25e1d1a7097f30c7caefc7d07f5efc216727d9595749698f69ba2d3f3c9ac6ce`  
		Last Modified: Thu, 04 Dec 2025 03:07:31 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:fe601bbe28b63642b9b52b7a8478c09ad9007efb3307344dd0200e78ec89757d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128099244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11f21ae0c179baf1e0e49afea4c0c666026627f1546ff28efe88908b2a166f0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:50 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:06 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecc931e2191125378a0a9477c160a961192f08243ea2c2456849e3d27e222e0`  
		Last Modified: Wed, 03 Dec 2025 23:23:08 GMT  
		Size: 8.1 MB (8140516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce9f0fdd9a6972893cb9174962100c606a4ec4f96d43c364367a47626fdf9c`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878cfd957acc34a77a945074318f634f0e69a7c824871f6464251ac78b8a664e`  
		Last Modified: Wed, 03 Dec 2025 23:23:05 GMT  
		Size: 17.6 MB (17560711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff31c3c1cf921e42759f6740e9e0beef431a103e7e0a8d4cc77746069baa2a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57a283bca5c3cafa94cf6aa030b368473a528c61badf87a6acd532479536a3a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 10.2 MB (10195775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d43044fe88440c59cb4d09b26744e4f2a4765098262deecb118d338ea56699`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f15be6ca380c49f5c3b6f9788835a7f811e9ff6921a5c39692cb64255b1572`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2803db336c739715d724a2b06fa65fa1849d95ef8c19e34880c5b5acbc35d88`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f931e0fd6111c2578d5d9a54292a9dfec958fe94d1e7f68f1b31d197a333985`  
		Last Modified: Thu, 04 Dec 2025 00:09:27 GMT  
		Size: 7.2 MB (7230286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc7b8d7478ef5f2f5ba1e5db11c0fc93bd20eafe6b7606d9d47bf2331a2b3c`  
		Last Modified: Thu, 04 Dec 2025 00:09:28 GMT  
		Size: 90.0 KB (89955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d076abb53c41564afd763287157cf740f81e0db1053596ab43b14cd7ef71b07d`  
		Last Modified: Thu, 04 Dec 2025 00:09:25 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a101330bea32635e63394dee524dbef13c06b88980cbb82594b56006da57986`  
		Last Modified: Thu, 04 Dec 2025 00:09:31 GMT  
		Size: 59.9 MB (59893215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc26c05faa4dc67c6281383dfb1b858e05d90847279c446859a199658f586ac2`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdb33cb903b3e7bbad1c970a6cad894a4a031db43544a2245b7413b8146a78f`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:d42c8cf8a28b5613be8a5e682d1f0adc2a66593fc5825c921cbeb79908537a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c000f8f0e671395bd4558756b0240d013b2b9f86f582f6aebdb340e1c0bde`

```dockerfile
```

-	Layers:
	-	`sha256:c8b0bc7a5fcd7022ef2328012ba0f8cd8d24946692ba523f6780c59afcf2c0c5`  
		Last Modified: Thu, 04 Dec 2025 03:07:33 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:3b20b2f3273127bc77b0d5a10d6c89fbe489c6e26aabfcf70374718b183dfaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126234834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30509973b0ac1a4da60db5cd58eafc1683ae159d63618ea8b33fac2fea969ec9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:31 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:32 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935a3faa05b5054eb2d5539416291930c560ec5c5562fc406afa35bd473fb0e6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 7.5 MB (7461370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde152eb030abb1c199a35f2e9e0e6b1b6a57d4feb903df63b11037fac1a2ce6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f06bd5e7fd9b6ded91c70f08fd128821578ffc9820598e8f07b40cfb0d9ce5`  
		Last Modified: Wed, 03 Dec 2025 23:23:55 GMT  
		Size: 17.6 MB (17550088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afc00eecc90cef8da7558059bc5d03c4e8a6fcc711de9e737079165e731684`  
		Last Modified: Wed, 03 Dec 2025 23:23:50 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515c94502ad1a992ad7e0b00b558d157c6f159b4e9db4d9d2f40e7bafb17b92e`  
		Last Modified: Wed, 03 Dec 2025 23:23:52 GMT  
		Size: 10.2 MB (10188522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bee705c92c06181488e34193ffad6a12b619e780a07b1a79299bf5f0145f4d`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a23011c0e0e10c3d92ecd1d44a351ea1c7caa7b8dd85a808ee2e3d7b21fb6f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa197bf85b5aea7f0c51679266daa38199c6e7991b49320c5c16206a14c279f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3c3136863c024060420d7807c203025bc548ac5ad2b0858e446809ab410c`  
		Last Modified: Thu, 04 Dec 2025 00:09:54 GMT  
		Size: 6.5 MB (6538168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f77e8b986e32956581155ff6b177404ce1edb49d73437dd38ef58279f920ef`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 86.4 KB (86396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348c52291ee0284e8483fdfff7481d25d34bb401399ce821ec03bcb55d4d2e94`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018fd645a77660c02db5a21d598961bc1ed40e8aa011a2c6590fef87930aa5e`  
		Last Modified: Thu, 04 Dec 2025 00:09:57 GMT  
		Size: 59.7 MB (59725684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daf7cac083af2912d7cad82e45f8086baaba542e7e0aa6d43a21ce73dff00c`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88842983720a1ed7d8aa571666aff44394345c26366bf0d54590b6ff3eda3a84`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:9960273ea153bbe574b692c69e822b3013ee15f4c6c70e6a909ca44ec1ab3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1927298a387e339d847056a865f7134a8cfc0b73ce2d584fdaf95fa1bc81a8`

```dockerfile
```

-	Layers:
	-	`sha256:6007395b9d82e0ffe5855b313e61375469e3ae796653dc07903f13486fc11870`  
		Last Modified: Thu, 04 Dec 2025 03:07:36 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7c26d2db80935c936465085344b49347e1a3d64aab63c61dde7cb47fb85b0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125991288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb84df0944fb8b77d9caae220f0fe4e6533a8b0bb7ac9d1fe0ab537611d7539`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:fff37f801a284572fb4ec647febb83d21fa848330ad16164593fd754054e4e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eda8b90f0af1ce070ab1b486d36a6f8e52a00099f86dff74b9ede6cbeb4d19c`

```dockerfile
```

-	Layers:
	-	`sha256:7f49d359152acc433dd0182ab053b3a9885e5cbd5434e49990d59ff25fc3a484`  
		Last Modified: Thu, 04 Dec 2025 03:07:40 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:421dffbe324135321070051128d9d2787f0465a94d728070953b89255438a5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:353a1727d0e6ac8343824427ff6d442390472e0bb77ca01655da0ddcf51fb9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156655034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfdf4d733c409824955ff98bc575e0384deb01f66c4f8e9a244e158f749ea1f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
# Thu, 04 Dec 2025 00:34:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 00:34:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 00:34:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 00:34:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91aa056e56aa4a66ab4445fc928d9900f02526039d0d9e034dbd5f1864ded0e`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 3.4 MB (3398378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ba6b907925696d4f4bf8e90017155cfc57c2eb3a3daf7b148f8e03ec3e6e46`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa8d4bd6998c2fe7060be7b4c380915afb0718f2a048cffec66cfa2b3396679`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb4f0a9a116b4469861628ca4fa5396cf4046b9589a4d19291e11bfea5fc4c6`  
		Last Modified: Thu, 04 Dec 2025 00:34:49 GMT  
		Size: 17.4 MB (17370975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0121931059414c5b535a820a06149e50072743b8d7d9d1292e94b5dd7cde587f`  
		Last Modified: Thu, 04 Dec 2025 00:34:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4b08832b0e539cc368981d37d867659cadd73c07d5b17094e24239509d6d408f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2014725d32624c20c843af1525ac27aa85a87442225e3a832e40bb9658fa40`

```dockerfile
```

-	Layers:
	-	`sha256:d430a287400d6e64aca730c1235ea91292ca5733da9bb24288faf42078d9d405`  
		Last Modified: Thu, 04 Dec 2025 03:07:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a1db98f222784429b330f778f1957ad3018c290fa95637335ca9ee58c09bd1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147091297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c01b600ca0f7971b32388b10745a1245988aa3e8ca83212a3ea4c2b2eb9609c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
# Thu, 04 Dec 2025 00:34:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 00:34:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 00:34:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 00:34:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29744f0d4e84a604abd643d72e500a942b93b47aebc9608aeb11c9547505978f`  
		Last Modified: Thu, 04 Dec 2025 00:34:30 GMT  
		Size: 3.4 MB (3389949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd8dfe81186ff0b816407ebca7cde7473e4568a00053e41a9b865506bb318b0`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334d36e8d2a2055d1ce374a4db658c40f1524af962083d9b5da52852d76a46cd`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0acb58cf5a910482ee59a629e47ddf2882796d6846f7fcba3860c753046c3`  
		Last Modified: Thu, 04 Dec 2025 00:34:29 GMT  
		Size: 17.7 MB (17708720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68ee96465b587d4e1d201671d6f38af93ce12e3e8de1e4318ce20a9a3a22aa5`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:629ac163c9e7113117c78d53db8ab7c25aba4ee3de17c2844199d515d03b1900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63d85a6970c712972dadb4c3f5562f4814c08c63e23177be3b9fb30441e0646`

```dockerfile
```

-	Layers:
	-	`sha256:a9a45b6a9af3185edc3fef012c4ee2bbc1e2310c25a9b46260487d287c102821`  
		Last Modified: Thu, 04 Dec 2025 03:08:01 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:d47faf85fc5cb4283d7a20c95b6b02d012250b46ec26567554076e2767cb9093
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
$ docker pull docker@sha256:402b891668de1fe99eb7d054cf25df00a6217232585c02a509ecd7d89ee90856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135884343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b4440e17e983942d30f645a848d94efafacaef8be8733a99feeedc93b05165`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:730e45afac3924277c2d3d65bbd80e18019ece14ae5ca8ec59a55372c9357de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4237c7596712be121f7d034be83210391de8307b0ad7f32c6a82e65b63cd5899`

```dockerfile
```

-	Layers:
	-	`sha256:25e1d1a7097f30c7caefc7d07f5efc216727d9595749698f69ba2d3f3c9ac6ce`  
		Last Modified: Thu, 04 Dec 2025 03:07:31 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:fe601bbe28b63642b9b52b7a8478c09ad9007efb3307344dd0200e78ec89757d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128099244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11f21ae0c179baf1e0e49afea4c0c666026627f1546ff28efe88908b2a166f0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:46 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:50 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:06 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:06 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecc931e2191125378a0a9477c160a961192f08243ea2c2456849e3d27e222e0`  
		Last Modified: Wed, 03 Dec 2025 23:23:08 GMT  
		Size: 8.1 MB (8140516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce9f0fdd9a6972893cb9174962100c606a4ec4f96d43c364367a47626fdf9c`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878cfd957acc34a77a945074318f634f0e69a7c824871f6464251ac78b8a664e`  
		Last Modified: Wed, 03 Dec 2025 23:23:05 GMT  
		Size: 17.6 MB (17560711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff31c3c1cf921e42759f6740e9e0beef431a103e7e0a8d4cc77746069baa2a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57a283bca5c3cafa94cf6aa030b368473a528c61badf87a6acd532479536a3a`  
		Last Modified: Wed, 03 Dec 2025 23:23:06 GMT  
		Size: 10.2 MB (10195775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d43044fe88440c59cb4d09b26744e4f2a4765098262deecb118d338ea56699`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f15be6ca380c49f5c3b6f9788835a7f811e9ff6921a5c39692cb64255b1572`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2803db336c739715d724a2b06fa65fa1849d95ef8c19e34880c5b5acbc35d88`  
		Last Modified: Wed, 03 Dec 2025 23:23:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f931e0fd6111c2578d5d9a54292a9dfec958fe94d1e7f68f1b31d197a333985`  
		Last Modified: Thu, 04 Dec 2025 00:09:27 GMT  
		Size: 7.2 MB (7230286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc7b8d7478ef5f2f5ba1e5db11c0fc93bd20eafe6b7606d9d47bf2331a2b3c`  
		Last Modified: Thu, 04 Dec 2025 00:09:28 GMT  
		Size: 90.0 KB (89955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d076abb53c41564afd763287157cf740f81e0db1053596ab43b14cd7ef71b07d`  
		Last Modified: Thu, 04 Dec 2025 00:09:25 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a101330bea32635e63394dee524dbef13c06b88980cbb82594b56006da57986`  
		Last Modified: Thu, 04 Dec 2025 00:09:31 GMT  
		Size: 59.9 MB (59893215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc26c05faa4dc67c6281383dfb1b858e05d90847279c446859a199658f586ac2`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdb33cb903b3e7bbad1c970a6cad894a4a031db43544a2245b7413b8146a78f`  
		Last Modified: Thu, 04 Dec 2025 00:09:26 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:d42c8cf8a28b5613be8a5e682d1f0adc2a66593fc5825c921cbeb79908537a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c000f8f0e671395bd4558756b0240d013b2b9f86f582f6aebdb340e1c0bde`

```dockerfile
```

-	Layers:
	-	`sha256:c8b0bc7a5fcd7022ef2328012ba0f8cd8d24946692ba523f6780c59afcf2c0c5`  
		Last Modified: Thu, 04 Dec 2025 03:07:33 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:3b20b2f3273127bc77b0d5a10d6c89fbe489c6e26aabfcf70374718b183dfaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126234834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30509973b0ac1a4da60db5cd58eafc1683ae159d63618ea8b33fac2fea969ec9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:28 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:31 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:32 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935a3faa05b5054eb2d5539416291930c560ec5c5562fc406afa35bd473fb0e6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 7.5 MB (7461370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde152eb030abb1c199a35f2e9e0e6b1b6a57d4feb903df63b11037fac1a2ce6`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f06bd5e7fd9b6ded91c70f08fd128821578ffc9820598e8f07b40cfb0d9ce5`  
		Last Modified: Wed, 03 Dec 2025 23:23:55 GMT  
		Size: 17.6 MB (17550088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afc00eecc90cef8da7558059bc5d03c4e8a6fcc711de9e737079165e731684`  
		Last Modified: Wed, 03 Dec 2025 23:23:50 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515c94502ad1a992ad7e0b00b558d157c6f159b4e9db4d9d2f40e7bafb17b92e`  
		Last Modified: Wed, 03 Dec 2025 23:23:52 GMT  
		Size: 10.2 MB (10188522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bee705c92c06181488e34193ffad6a12b619e780a07b1a79299bf5f0145f4d`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a23011c0e0e10c3d92ecd1d44a351ea1c7caa7b8dd85a808ee2e3d7b21fb6f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa197bf85b5aea7f0c51679266daa38199c6e7991b49320c5c16206a14c279f`  
		Last Modified: Wed, 03 Dec 2025 23:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3c3136863c024060420d7807c203025bc548ac5ad2b0858e446809ab410c`  
		Last Modified: Thu, 04 Dec 2025 00:09:54 GMT  
		Size: 6.5 MB (6538168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f77e8b986e32956581155ff6b177404ce1edb49d73437dd38ef58279f920ef`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 86.4 KB (86396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348c52291ee0284e8483fdfff7481d25d34bb401399ce821ec03bcb55d4d2e94`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018fd645a77660c02db5a21d598961bc1ed40e8aa011a2c6590fef87930aa5e`  
		Last Modified: Thu, 04 Dec 2025 00:09:57 GMT  
		Size: 59.7 MB (59725684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daf7cac083af2912d7cad82e45f8086baaba542e7e0aa6d43a21ce73dff00c`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88842983720a1ed7d8aa571666aff44394345c26366bf0d54590b6ff3eda3a84`  
		Last Modified: Thu, 04 Dec 2025 00:09:53 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:9960273ea153bbe574b692c69e822b3013ee15f4c6c70e6a909ca44ec1ab3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1927298a387e339d847056a865f7134a8cfc0b73ce2d584fdaf95fa1bc81a8`

```dockerfile
```

-	Layers:
	-	`sha256:6007395b9d82e0ffe5855b313e61375469e3ae796653dc07903f13486fc11870`  
		Last Modified: Thu, 04 Dec 2025 03:07:36 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7c26d2db80935c936465085344b49347e1a3d64aab63c61dde7cb47fb85b0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125991288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb84df0944fb8b77d9caae220f0fe4e6533a8b0bb7ac9d1fe0ab537611d7539`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:fff37f801a284572fb4ec647febb83d21fa848330ad16164593fd754054e4e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eda8b90f0af1ce070ab1b486d36a6f8e52a00099f86dff74b9ede6cbeb4d19c`

```dockerfile
```

-	Layers:
	-	`sha256:7f49d359152acc433dd0182ab053b3a9885e5cbd5434e49990d59ff25fc3a484`  
		Last Modified: Thu, 04 Dec 2025 03:07:40 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:0eb975351ee9df33c41e2946cbd2143ba55fac8ae27c448d9b3fdbd060e969a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:dcd91f0a9029b88613dc48540fe8c128b08bff07dd8b99f4f0242513176f5297
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3290731333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799920065e3e5f973ef96625fe4937bc2563ef5a8e33a59bcf9de238cabe02f5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 23:27:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:45 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:19 GMT
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
	-	`sha256:d7146b17b5860acc8808e415263a03814888a80daaac674aad997e45e4815684`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcde76394ea2b592fadc80c106462452d55b0d2db294199cd06e6368a24364c`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 399.7 KB (399722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620bb71f2687fad09692e4f84af86fcfcccd93276ea8697e98e13c65e534b9c3`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465405d75d81f743b9557eef457a787436466226d68ca5613d82a7c0b02a84d2`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07117c52ec04e5430ba6c16b89755a395af5dc950c1e1965c1522e0b6c7c9369`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 19.5 MB (19450943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3e1dd17fe0599cd773fe8876a3468ed2785a46b58b877ece7fd1b58b174a22`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb064c05a6de4303a29f355e360b69a0b4018d7f54aadc58e85ed89554d726c`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986e5dffed43d7b98b12e2629e4811443a52b3b642ca30a1a9cd58487af9617`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b3176876e2fd382f76e0a0f989cf351e47e43b0507d7e9d91f5846ac99ea9`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 23.9 MB (23949262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591161397992bd49794d31aa33971c487096caccf147b7786c1e0a755a9fe805`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5d7df70beef98e61be396a7a9c43f445629c0394d49ad6b7245913efaf99a2`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e81f136de465956899822ab4c68c183a31a5a4568f59543513268a0cd87b4`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c959e0b45832e9394f8ced26f7a951cfa65a205041622a521e760b10428ac80`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 11.5 MB (11463861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:e510d0ffbc8c058424c173f9fdc8cf04cc404418596a5affa555804099d86454
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1825263813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f07aa98e515049fbc2b1e495db11a4b0d477c90d0af1e624c7091898258e4fa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Wed, 03 Dec 2025 23:27:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:29 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:28:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:28:55 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:22 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:37 GMT
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
	-	`sha256:f95ab1d322f7331427de0527a98516714be5fdfab8001a0c3afbfdd375f8c704`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997dee9e9b12bed5bc50b78d9d4a23fa986d3c820f38741c6df0273e145b4228`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 501.4 KB (501396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8221a12dd08308b3b8cd4120faa67fcdef9df7d39a4a7acd1474ee4b616290`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88be20e3446295169e1821cf2636d87b5284dd5ea89d65f2b8d6928855ae5b8`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8279728faba290f6ba2b243e3e21a5a11dec89f4ef7ce8e21bc6efb45beb59`  
		Last Modified: Wed, 03 Dec 2025 23:41:22 GMT  
		Size: 19.4 MB (19424449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0ef6633566397de87875a06aae522041d6e3b3a4004ac25a21f129c00b741f`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a349148f8226a779c9bac7fe27b9bb6662d9f5d28cb22d5969722e7e79b280`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4c28f07a327eb3afb667f83caa8e98c39382dcf476cbc17b52e84e0a43092b`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6508f164b53e8ff2ae3c44be363df93cbfcb58724fadaeae0c3dc1170b3acd`  
		Last Modified: Wed, 03 Dec 2025 23:41:23 GMT  
		Size: 23.9 MB (23925342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb3468481b597bde6c2cf074d7b9737c7a77424f16922fbc386ea348e80025`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f80013208797c388923aa4d38cbea4495d3ea0c614ed53a2293f41f22d21a84`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187a71b662b80ffd9fe1339b7e7d5cbff0079de921771aac208a9b839ae48b2`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be497084a394b66ecc710847dddcef4176a5a319c37cb4b40d904e72c8c9a5`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 11.4 MB (11439399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:983813a6983c58f428973a22873ce9e8091209be5490d03e1b2b1a61196967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:e510d0ffbc8c058424c173f9fdc8cf04cc404418596a5affa555804099d86454
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1825263813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f07aa98e515049fbc2b1e495db11a4b0d477c90d0af1e624c7091898258e4fa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Wed, 03 Dec 2025 23:27:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:29 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:28:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:28:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:28:55 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:22 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:37 GMT
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
	-	`sha256:f95ab1d322f7331427de0527a98516714be5fdfab8001a0c3afbfdd375f8c704`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997dee9e9b12bed5bc50b78d9d4a23fa986d3c820f38741c6df0273e145b4228`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 501.4 KB (501396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8221a12dd08308b3b8cd4120faa67fcdef9df7d39a4a7acd1474ee4b616290`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88be20e3446295169e1821cf2636d87b5284dd5ea89d65f2b8d6928855ae5b8`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8279728faba290f6ba2b243e3e21a5a11dec89f4ef7ce8e21bc6efb45beb59`  
		Last Modified: Wed, 03 Dec 2025 23:41:22 GMT  
		Size: 19.4 MB (19424449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0ef6633566397de87875a06aae522041d6e3b3a4004ac25a21f129c00b741f`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a349148f8226a779c9bac7fe27b9bb6662d9f5d28cb22d5969722e7e79b280`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4c28f07a327eb3afb667f83caa8e98c39382dcf476cbc17b52e84e0a43092b`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6508f164b53e8ff2ae3c44be363df93cbfcb58724fadaeae0c3dc1170b3acd`  
		Last Modified: Wed, 03 Dec 2025 23:41:23 GMT  
		Size: 23.9 MB (23925342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb3468481b597bde6c2cf074d7b9737c7a77424f16922fbc386ea348e80025`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f80013208797c388923aa4d38cbea4495d3ea0c614ed53a2293f41f22d21a84`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187a71b662b80ffd9fe1339b7e7d5cbff0079de921771aac208a9b839ae48b2`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be497084a394b66ecc710847dddcef4176a5a319c37cb4b40d904e72c8c9a5`  
		Last Modified: Wed, 03 Dec 2025 23:41:21 GMT  
		Size: 11.4 MB (11439399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:2d936418a8c21ad8678fc7b3af4cbb724a2ea1347653cbac3ad6603facd89118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:dcd91f0a9029b88613dc48540fe8c128b08bff07dd8b99f4f0242513176f5297
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3290731333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799920065e3e5f973ef96625fe4937bc2563ef5a8e33a59bcf9de238cabe02f5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 23:27:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 23:28:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Dec 2025 23:28:45 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:28:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Wed, 03 Dec 2025 23:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 03 Dec 2025 23:29:01 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 03 Dec 2025 23:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 03 Dec 2025 23:29:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 03 Dec 2025 23:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 03 Dec 2025 23:29:19 GMT
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
	-	`sha256:d7146b17b5860acc8808e415263a03814888a80daaac674aad997e45e4815684`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcde76394ea2b592fadc80c106462452d55b0d2db294199cd06e6368a24364c`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 399.7 KB (399722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620bb71f2687fad09692e4f84af86fcfcccd93276ea8697e98e13c65e534b9c3`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465405d75d81f743b9557eef457a787436466226d68ca5613d82a7c0b02a84d2`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07117c52ec04e5430ba6c16b89755a395af5dc950c1e1965c1522e0b6c7c9369`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 19.5 MB (19450943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3e1dd17fe0599cd773fe8876a3468ed2785a46b58b877ece7fd1b58b174a22`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb064c05a6de4303a29f355e360b69a0b4018d7f54aadc58e85ed89554d726c`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986e5dffed43d7b98b12e2629e4811443a52b3b642ca30a1a9cd58487af9617`  
		Last Modified: Wed, 03 Dec 2025 23:46:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b3176876e2fd382f76e0a0f989cf351e47e43b0507d7e9d91f5846ac99ea9`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 23.9 MB (23949262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591161397992bd49794d31aa33971c487096caccf147b7786c1e0a755a9fe805`  
		Last Modified: Wed, 03 Dec 2025 23:47:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5d7df70beef98e61be396a7a9c43f445629c0394d49ad6b7245913efaf99a2`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e81f136de465956899822ab4c68c183a31a5a4568f59543513268a0cd87b4`  
		Last Modified: Wed, 03 Dec 2025 23:46:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c959e0b45832e9394f8ced26f7a951cfa65a205041622a521e760b10428ac80`  
		Last Modified: Wed, 03 Dec 2025 23:46:58 GMT  
		Size: 11.5 MB (11463861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
