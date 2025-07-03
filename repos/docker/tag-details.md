<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.3`](#docker283)
-	[`docker:28.3-cli`](#docker283-cli)
-	[`docker:28.3-dind`](#docker283-dind)
-	[`docker:28.3-dind-rootless`](#docker283-dind-rootless)
-	[`docker:28.3-windowsservercore`](#docker283-windowsservercore)
-	[`docker:28.3-windowsservercore-ltsc2022`](#docker283-windowsservercore-ltsc2022)
-	[`docker:28.3-windowsservercore-ltsc2025`](#docker283-windowsservercore-ltsc2025)
-	[`docker:28.3.1`](#docker2831)
-	[`docker:28.3.1-alpine3.22`](#docker2831-alpine322)
-	[`docker:28.3.1-cli`](#docker2831-cli)
-	[`docker:28.3.1-cli-alpine3.22`](#docker2831-cli-alpine322)
-	[`docker:28.3.1-dind`](#docker2831-dind)
-	[`docker:28.3.1-dind-alpine3.22`](#docker2831-dind-alpine322)
-	[`docker:28.3.1-dind-rootless`](#docker2831-dind-rootless)
-	[`docker:28.3.1-windowsservercore`](#docker2831-windowsservercore)
-	[`docker:28.3.1-windowsservercore-ltsc2022`](#docker2831-windowsservercore-ltsc2022)
-	[`docker:28.3.1-windowsservercore-ltsc2025`](#docker2831-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:0a2ee60851e1b61a54707476526c4ed48cc55641a17a5cba8a77fb78e7a4742c
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
$ docker pull docker@sha256:af6f4a6f99d3b928aaf2a4c89c92362b61fe5714ce4b359357a7034d72addbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147530306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56629b96a64d6e6a67bb353c4659a5b6bcbe3d1b5d839623c78e3fbfb5d5d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:f284b77d89a52d6e50f665a70dc9cba7676d350135900856dffad8fa83381129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a60b03d224867bf21b8fcdbedf71f4b988ef38df593113cf167071ae0db1ba`

```dockerfile
```

-	Layers:
	-	`sha256:de6313881469a25f3e98fd3e7a03e6f441046c278766a4991497c229caa95ca8`  
		Last Modified: Thu, 03 Jul 2025 20:07:32 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:1a2b90b79d231f6d79b223f7f6148732566e4f6c8051b02ed9dbb8442cfcd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138128973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7996c20d4b7e0501900c77f11b3517bdde8df963fd95bca52f74102cbee16037`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c35411abd7ff8741d102086e57d13dcf53a36b38d0f83d70dfc564451c476f`  
		Last Modified: Thu, 03 Jul 2025 18:07:38 GMT  
		Size: 9.5 MB (9461151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4334023f752ea84943589c958d76280ad68320a22b65a8b28032bfef145a87`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 90.1 KB (90064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6838b2f15e318a3756e830fe9328c98594e76f559f183a6a2a82f247414e7`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af830fec2f9b00ff6031aa3b5abf77926f1f8ec61c43c2fd933a53aeec3b9716`  
		Last Modified: Thu, 03 Jul 2025 18:07:40 GMT  
		Size: 58.2 MB (58196228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caaa15e0a3e27f74ea0cdc96286507cdae37c6b9da9f6dd58b75262174e04c`  
		Last Modified: Thu, 03 Jul 2025 18:07:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5519b7b6fb48cbf0f06bcb48d96dac6ae50d2f29df217e3ed905c33cfab0f0ff`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:9fbda7207e684fc22b48dcb3d1cb9b90be4e59a79e8f051557e013f5098a80e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f6cfed87f8a2540111bff41a1e80f225970a9299f983f4513c8cb7bc11b3d3`

```dockerfile
```

-	Layers:
	-	`sha256:cefef8bf5e16c3e687c0fa2dec76440f45a5dfecfd26a50caecaeff9ca6c7528`  
		Last Modified: Thu, 03 Jul 2025 20:07:36 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:73e517576082f7d56a5d5d498e3213393339b90ec3f7b5716b77e74da9a7dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136275323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e52499045af79026f3a96eb634a83bcbfcc05f78d5156c2a02d7d17434ed51`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8283e24f943182f28dc30d039850e13d96eafad82bb6c22a140c3efe652058c1`  
		Last Modified: Thu, 03 Jul 2025 18:08:05 GMT  
		Size: 8.6 MB (8610439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450a67de7fa2fbc5711e2fdfa60c7a2945e5a35ffe63f7bc37853d0460923`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 86.5 KB (86500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9b557ed7aa7cbe6b15891cd15a970a5153869d665c096b93ce12aba19709c`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5256c88f5ca619407e171fec8e2327d32bdbb28ff0039389c324c0957d51e2a7`  
		Last Modified: Thu, 03 Jul 2025 18:08:13 GMT  
		Size: 58.2 MB (58196195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5ad95ba8e852e939d06670a567addbe1f7545dfcf9cc2f0bc72df2a549f192`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9ec3f7bf60f8287e8fb6b564e36112f40c678b0a2419e630d97e2eee47d12`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:676399e8815c91e2f684422dcc72561d36f8b71d0a31afa4f8167e54862d165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47da4f2e8332513e7f2fd9f4207d0b2046cb012304e8af3010c40bc64f11e5e8`

```dockerfile
```

-	Layers:
	-	`sha256:e377a69875e60adb621efef5a8aca158b3dafb7230b4f16619be0970236a7d43`  
		Last Modified: Thu, 03 Jul 2025 20:07:39 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9091b93a0497a742433859af71e9d2cbf91a04b4f8b463b2a3ac7bccf626b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138567854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7777fe83512e386382fb92ecdee5fab02657d37d0e4f5c421aa77b3a7e64c3b6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:0a04bc025db0198b912fa1aaba813b1f2e18956dd246940e2a1e7fc2edc56a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b366a219a7150c173e76372f82ae9e34c8c02de7aa62cb30dd1b0d33c196573c`

```dockerfile
```

-	Layers:
	-	`sha256:3650e92878e003d91cb996c90670a5c4fc7f62157f8338da233bf84fee665245`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:d623d8d72aa526abcdc996ac8963062a715235ffda58556d864112b8b3fab21b
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
$ docker pull docker@sha256:85b2b37853090b68f2bec9b58a28c514aa4a92821231590662d961ec69ca3bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75408319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0884f72ce3334bfac5c84db32abe1dbd7d6d3b0eaeda1735e8e1c5017582741b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6e8ad138fd78450c30c813f8090cdde12769d5d73beb9c3074783e319a24839d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bceb0017eb30fe94b56cfaebf3348fa544b1440eda09cd6afd8a01f4111633`

```dockerfile
```

-	Layers:
	-	`sha256:665d67252df18d6a5da27a11150b2176a16e3ccfa6892683968a9bd2c30e670c`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a3adc3151b74ccad480eee90a0785c6bbf00ae197b29da17912540a9c6307df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70375532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17419babf75f830d0703a82c44c1ea73abe9ad55bc6ecf940e7b6094ace9dff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:26df6789e84e297b20d944fb722165f5a370ea64e3feab5f200814bcebda2025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0fbbe78fe8f5212ac315d751f274fb1730455ffc3833b07d1aeddd8de82656`

```dockerfile
```

-	Layers:
	-	`sha256:1ffa78e1803982dfe37ed32d4c1bd928dfb46888778cd8bf093da83cd5b55b46`  
		Last Modified: Thu, 03 Jul 2025 20:07:47 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c6088237d22ce9f1c74b09f299ffc9f660ae3d9b0b05cf68e70974559ef0b72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69376189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10eeb922114f57e5118d438eef0c96af65407b628eafbe137c8fdb51fcad1d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4620cfbab6b718b6d7608e646d78fee8bd24e4a9e3998c00d2cdb9fc500a4d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0119c9efe61eb4c2a2315fc24b97f0186bdecc9db92ff39c084e27c154054af`

```dockerfile
```

-	Layers:
	-	`sha256:5ab8fb7ac3eb539be8a1207dcaf14c686d92029c58cf5144592f402daaafb75b`  
		Last Modified: Thu, 03 Jul 2025 20:07:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:345329b66e3b117cfabf618ee56c67a4ce9ee4226ed3bf4b2b62d98e8d15e90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7302f18f8f6a2df7421bf64634eb1a82bab0d8397a5cfeed34f49ad79288594d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6972a69e584db7ee5fb8279874ef80ea710672907c48d4e75432ecec12a692bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36eae856160dae536d39b9a3894bcdd53e6a8515faedf00b3ed1d0b03dff1a6`

```dockerfile
```

-	Layers:
	-	`sha256:1202a1d5f73476f0c58ffdbc17ef1175dc800026e4e305fffb0e8a8f847c4234`  
		Last Modified: Thu, 03 Jul 2025 20:07:57 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:0a2ee60851e1b61a54707476526c4ed48cc55641a17a5cba8a77fb78e7a4742c
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
$ docker pull docker@sha256:af6f4a6f99d3b928aaf2a4c89c92362b61fe5714ce4b359357a7034d72addbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147530306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56629b96a64d6e6a67bb353c4659a5b6bcbe3d1b5d839623c78e3fbfb5d5d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f284b77d89a52d6e50f665a70dc9cba7676d350135900856dffad8fa83381129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a60b03d224867bf21b8fcdbedf71f4b988ef38df593113cf167071ae0db1ba`

```dockerfile
```

-	Layers:
	-	`sha256:de6313881469a25f3e98fd3e7a03e6f441046c278766a4991497c229caa95ca8`  
		Last Modified: Thu, 03 Jul 2025 20:07:32 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1a2b90b79d231f6d79b223f7f6148732566e4f6c8051b02ed9dbb8442cfcd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138128973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7996c20d4b7e0501900c77f11b3517bdde8df963fd95bca52f74102cbee16037`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c35411abd7ff8741d102086e57d13dcf53a36b38d0f83d70dfc564451c476f`  
		Last Modified: Thu, 03 Jul 2025 18:07:38 GMT  
		Size: 9.5 MB (9461151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4334023f752ea84943589c958d76280ad68320a22b65a8b28032bfef145a87`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 90.1 KB (90064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6838b2f15e318a3756e830fe9328c98594e76f559f183a6a2a82f247414e7`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af830fec2f9b00ff6031aa3b5abf77926f1f8ec61c43c2fd933a53aeec3b9716`  
		Last Modified: Thu, 03 Jul 2025 18:07:40 GMT  
		Size: 58.2 MB (58196228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caaa15e0a3e27f74ea0cdc96286507cdae37c6b9da9f6dd58b75262174e04c`  
		Last Modified: Thu, 03 Jul 2025 18:07:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5519b7b6fb48cbf0f06bcb48d96dac6ae50d2f29df217e3ed905c33cfab0f0ff`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9fbda7207e684fc22b48dcb3d1cb9b90be4e59a79e8f051557e013f5098a80e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f6cfed87f8a2540111bff41a1e80f225970a9299f983f4513c8cb7bc11b3d3`

```dockerfile
```

-	Layers:
	-	`sha256:cefef8bf5e16c3e687c0fa2dec76440f45a5dfecfd26a50caecaeff9ca6c7528`  
		Last Modified: Thu, 03 Jul 2025 20:07:36 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:73e517576082f7d56a5d5d498e3213393339b90ec3f7b5716b77e74da9a7dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136275323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e52499045af79026f3a96eb634a83bcbfcc05f78d5156c2a02d7d17434ed51`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8283e24f943182f28dc30d039850e13d96eafad82bb6c22a140c3efe652058c1`  
		Last Modified: Thu, 03 Jul 2025 18:08:05 GMT  
		Size: 8.6 MB (8610439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450a67de7fa2fbc5711e2fdfa60c7a2945e5a35ffe63f7bc37853d0460923`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 86.5 KB (86500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9b557ed7aa7cbe6b15891cd15a970a5153869d665c096b93ce12aba19709c`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5256c88f5ca619407e171fec8e2327d32bdbb28ff0039389c324c0957d51e2a7`  
		Last Modified: Thu, 03 Jul 2025 18:08:13 GMT  
		Size: 58.2 MB (58196195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5ad95ba8e852e939d06670a567addbe1f7545dfcf9cc2f0bc72df2a549f192`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9ec3f7bf60f8287e8fb6b564e36112f40c678b0a2419e630d97e2eee47d12`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:676399e8815c91e2f684422dcc72561d36f8b71d0a31afa4f8167e54862d165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47da4f2e8332513e7f2fd9f4207d0b2046cb012304e8af3010c40bc64f11e5e8`

```dockerfile
```

-	Layers:
	-	`sha256:e377a69875e60adb621efef5a8aca158b3dafb7230b4f16619be0970236a7d43`  
		Last Modified: Thu, 03 Jul 2025 20:07:39 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9091b93a0497a742433859af71e9d2cbf91a04b4f8b463b2a3ac7bccf626b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138567854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7777fe83512e386382fb92ecdee5fab02657d37d0e4f5c421aa77b3a7e64c3b6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0a04bc025db0198b912fa1aaba813b1f2e18956dd246940e2a1e7fc2edc56a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b366a219a7150c173e76372f82ae9e34c8c02de7aa62cb30dd1b0d33c196573c`

```dockerfile
```

-	Layers:
	-	`sha256:3650e92878e003d91cb996c90670a5c4fc7f62157f8338da233bf84fee665245`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:b44749d9b6aba4f5f80bb759bb6ea83e62a1f2c8c0897ad059c5eeafb8d43c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:db4c04bc4465b0434d622bf882950ce45685a378b0ee811e9e1b1219ba6e9436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168515988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21511f843dd54e89f5b101840d8b53c72e1c5ddcd62a5f854485baaa6600fa9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b828347c2a041335957c90cb55b04a323af16f817d2ea2aaa04c38fd9e0a915b`  
		Last Modified: Thu, 03 Jul 2025 18:11:38 GMT  
		Size: 3.4 MB (3398182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9015f88f20407c97d95eec2557adffa39da70fe898e9ef54cc056e91f839250`  
		Last Modified: Thu, 03 Jul 2025 18:11:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fe64c2be9d18d459bedfb0eaae711ac691aae9da049d2259fa61694eebd252`  
		Last Modified: Thu, 03 Jul 2025 18:11:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6974db92eb03859ebac691c35b3b8e4bda756d27667351ec08ad27e3cebb426`  
		Last Modified: Thu, 03 Jul 2025 18:11:40 GMT  
		Size: 17.6 MB (17586158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69244f3e5323c1ad99d83700a10a30cbf3c9b59bd1d6deeb518016c91586411e`  
		Last Modified: Thu, 03 Jul 2025 18:11:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a0cc335b94ca365a19094d5303c10b30b5b1662788b30690d3a98d802427f0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d20f1d9888c19a6d1afdef8729e43aec20f90f322855e9b5c650247836ff0c`

```dockerfile
```

-	Layers:
	-	`sha256:e2532b0be60f5ccad634be0410f2b01c3922c3e42bfc227d2e206c65d2636109`  
		Last Modified: Thu, 03 Jul 2025 20:07:54 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5cedcdbd876edad79f8f62fec3ae650536577aa61a559acaa654dc6f6af631b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159976175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c81ca73fc3e1d219a425a73736a34d915776a8259e79eedd00597f482971cc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055439fa6d8fcc51af0c10bf7bc294b0e1f51845f1fdf975c6f2ed005a72dd7`  
		Last Modified: Thu, 03 Jul 2025 18:22:09 GMT  
		Size: 3.4 MB (3389671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5a4b35eded985f79fbbe8910bab2457acf21a3a5174dc98c50b5a52d6ae94c`  
		Last Modified: Thu, 03 Jul 2025 18:22:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a53aeca772b1453a3107bc47c8fa4c0a699b795f5bb46ce8147903629091105`  
		Last Modified: Thu, 03 Jul 2025 18:22:08 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae30160e013cd77a67fb1c70bca1161363b6d03b329bdbacdb070411f5fab194`  
		Last Modified: Thu, 03 Jul 2025 18:22:10 GMT  
		Size: 18.0 MB (18017309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156b018b4075be77289b3748988b7f34a0e22844508c688dcb3d3fbf47cba9c5`  
		Last Modified: Thu, 03 Jul 2025 18:22:08 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f92dbdaa152a7b0b5985bc9fb607ae59b1f53293d7e03ed0a763bfdb11d65c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e0049363c6bc42c7778de09c867a855ecc9d304eed6f5197c9c0be01a92207`

```dockerfile
```

-	Layers:
	-	`sha256:ddb6058b675b6f844f3eeb5728ee724318dd9b2b36a6a2ac8c90f51f2a3f80a3`  
		Last Modified: Thu, 03 Jul 2025 20:07:57 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:7bc3cbaeffb673a3857fad815ce1bc01a5ffe74778eeb337ad55c118c72f836a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:6fd3a0953d971332397c8e5f14fa538fc9feb8ee0df0761ef69cc664d2c15d5a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542412535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7fb045a7559131f0319249930363ace2c34f3549f5254f962c31ec2b021974`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 03 Jul 2025 17:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:28:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:28:01 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:28:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:28:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:28:17 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:28:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:28:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:28:30 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:28:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8360bc4e45fd1207fbb8507f009f2fafe0c692dda8013b87da385b1687fdb93`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee70f98e67bab9d88bef6785da7dcb0243c6678f90f98f1819bb1d6f15bc400`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 401.7 KB (401674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79844d9fe7e509cc013db5713ac75c91fdef2469815feec90b5b5ccad0760d`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6417f363ada4659759175f87056dac7cb772357f80f942c6f12d9c3a511ae2`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754e9768d552528080346d5f1236df2b7fec0cc26703a72181ab5c56597d3874`  
		Last Modified: Thu, 03 Jul 2025 17:32:16 GMT  
		Size: 20.9 MB (20869952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773798f77aa5f53805ec80969f800c997234c80e3eeaeb70915df160d58698d7`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08de61fa1493600c5c1abb22fb424babbd40f76e25bc0cb27af06a1e6826699`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9638f01c3683753b6296eba7747c7453af7e93065c1727c6b1c271fe3a9ad03`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2aa5bce1514c94a539188e90cbf3433418f9aee7b02aa6196d1b252701f4a6`  
		Last Modified: Thu, 03 Jul 2025 17:32:17 GMT  
		Size: 22.7 MB (22693614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b469a4641279b25c6f4c69230acb7f20cf78488659ef25e4b936f65ad62f7f`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94637a4a498775806b5d83e9b9a5dc8b4630e91f61f2560420791e57745cf4ff`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b5885e19d477e90daf5b71748592e75e7b6b7ff7acedc236c6872db6a7e27`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c38a51f4f1af8ed66ca040eb007a92422ee88d91d4dd660bd0f0f5214c46e7c`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 22.3 MB (22261431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:0dfbb2cb73e0f119f7827c4294818bae9e2b593f4f499366be7ab74496416a06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346334126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2405e622d57138fe3077ec39b9f3f42ebcd0cfdf09f47419ba243ae7fdd5b79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 03 Jul 2025 17:22:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:22:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:22:33 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:22:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:22:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:22:51 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:22:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:22:53 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:23:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:23:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:23:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:23:11 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:23:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b61b501a45983587b82cbf3ec9a02d5dc816be481f91442c358c854092ae35f`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f44a2afa65d60b4bf8e64db5fe87206c5d6caea4df5f91ab8520f7775c6108`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 361.4 KB (361411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a33626ee108dfe569f1ac806973edaad156af082da5adb5cdc619d671c92af`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415464cc927cf6550b8b02ab9a1c7d7076b523ce7f3eb3d6cb06af3cb0717cd`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece6c486f7a91317125ee5a8a9703bd97ad6fe62ffa3eed7300b64d6dae5658c`  
		Last Modified: Thu, 03 Jul 2025 17:23:46 GMT  
		Size: 20.8 MB (20833794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cca4e9c6c6042835085a7bec40bfedfff801d6a5bb1c55fd0d69f3cb4224c5`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e45039c40258e0ad1ddc66ea6789239b16daa6e4b25ad6133a2a0f9155e84e`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d056b131a087efcd1c66a659d7faab0e72b58a72df8d673e794b12df4133e2`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec084cd1ecfecc49f2aee4ece051aaf3b0e26d486dc4f206b8cdca3c459bbba3`  
		Last Modified: Thu, 03 Jul 2025 17:23:44 GMT  
		Size: 22.7 MB (22657606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746d4353372224213706d143dd92b6b6bb55a75ea19c08d8bf0a1831262fae78`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3131944c8f3aa2bfd1c82fa466a67d152080ddf612067169becafb202be3370`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbcaf71c6e95bc4ab5d255abea93afd44db0486b886ce5701bced2305375566`  
		Last Modified: Thu, 03 Jul 2025 17:23:43 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67da6c0deee4b547055907682ae68fc855d99f2e93d43f6e5b6959c0dd55db5e`  
		Last Modified: Thu, 03 Jul 2025 17:23:45 GMT  
		Size: 22.2 MB (22218098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3b16a51f7b350f70417bf9bd061388412d4fe13605c264cd3965ad44c040b98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:0dfbb2cb73e0f119f7827c4294818bae9e2b593f4f499366be7ab74496416a06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346334126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2405e622d57138fe3077ec39b9f3f42ebcd0cfdf09f47419ba243ae7fdd5b79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 03 Jul 2025 17:22:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:22:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:22:33 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:22:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:22:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:22:51 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:22:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:22:53 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:23:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:23:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:23:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:23:11 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:23:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b61b501a45983587b82cbf3ec9a02d5dc816be481f91442c358c854092ae35f`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f44a2afa65d60b4bf8e64db5fe87206c5d6caea4df5f91ab8520f7775c6108`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 361.4 KB (361411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a33626ee108dfe569f1ac806973edaad156af082da5adb5cdc619d671c92af`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415464cc927cf6550b8b02ab9a1c7d7076b523ce7f3eb3d6cb06af3cb0717cd`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece6c486f7a91317125ee5a8a9703bd97ad6fe62ffa3eed7300b64d6dae5658c`  
		Last Modified: Thu, 03 Jul 2025 17:23:46 GMT  
		Size: 20.8 MB (20833794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cca4e9c6c6042835085a7bec40bfedfff801d6a5bb1c55fd0d69f3cb4224c5`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e45039c40258e0ad1ddc66ea6789239b16daa6e4b25ad6133a2a0f9155e84e`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d056b131a087efcd1c66a659d7faab0e72b58a72df8d673e794b12df4133e2`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec084cd1ecfecc49f2aee4ece051aaf3b0e26d486dc4f206b8cdca3c459bbba3`  
		Last Modified: Thu, 03 Jul 2025 17:23:44 GMT  
		Size: 22.7 MB (22657606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746d4353372224213706d143dd92b6b6bb55a75ea19c08d8bf0a1831262fae78`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3131944c8f3aa2bfd1c82fa466a67d152080ddf612067169becafb202be3370`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbcaf71c6e95bc4ab5d255abea93afd44db0486b886ce5701bced2305375566`  
		Last Modified: Thu, 03 Jul 2025 17:23:43 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67da6c0deee4b547055907682ae68fc855d99f2e93d43f6e5b6959c0dd55db5e`  
		Last Modified: Thu, 03 Jul 2025 17:23:45 GMT  
		Size: 22.2 MB (22218098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:47e4025f5f5eb4bb57f9bc7b3c77d306050988fe620d7ee3e7af4720382fe323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:6fd3a0953d971332397c8e5f14fa538fc9feb8ee0df0761ef69cc664d2c15d5a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542412535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7fb045a7559131f0319249930363ace2c34f3549f5254f962c31ec2b021974`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 03 Jul 2025 17:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:28:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:28:01 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:28:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:28:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:28:17 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:28:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:28:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:28:30 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:28:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8360bc4e45fd1207fbb8507f009f2fafe0c692dda8013b87da385b1687fdb93`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee70f98e67bab9d88bef6785da7dcb0243c6678f90f98f1819bb1d6f15bc400`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 401.7 KB (401674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79844d9fe7e509cc013db5713ac75c91fdef2469815feec90b5b5ccad0760d`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6417f363ada4659759175f87056dac7cb772357f80f942c6f12d9c3a511ae2`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754e9768d552528080346d5f1236df2b7fec0cc26703a72181ab5c56597d3874`  
		Last Modified: Thu, 03 Jul 2025 17:32:16 GMT  
		Size: 20.9 MB (20869952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773798f77aa5f53805ec80969f800c997234c80e3eeaeb70915df160d58698d7`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08de61fa1493600c5c1abb22fb424babbd40f76e25bc0cb27af06a1e6826699`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9638f01c3683753b6296eba7747c7453af7e93065c1727c6b1c271fe3a9ad03`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2aa5bce1514c94a539188e90cbf3433418f9aee7b02aa6196d1b252701f4a6`  
		Last Modified: Thu, 03 Jul 2025 17:32:17 GMT  
		Size: 22.7 MB (22693614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b469a4641279b25c6f4c69230acb7f20cf78488659ef25e4b936f65ad62f7f`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94637a4a498775806b5d83e9b9a5dc8b4630e91f61f2560420791e57745cf4ff`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b5885e19d477e90daf5b71748592e75e7b6b7ff7acedc236c6872db6a7e27`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c38a51f4f1af8ed66ca040eb007a92422ee88d91d4dd660bd0f0f5214c46e7c`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 22.3 MB (22261431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3`

```console
$ docker pull docker@sha256:0a2ee60851e1b61a54707476526c4ed48cc55641a17a5cba8a77fb78e7a4742c
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

### `docker:28.3` - linux; amd64

```console
$ docker pull docker@sha256:af6f4a6f99d3b928aaf2a4c89c92362b61fe5714ce4b359357a7034d72addbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147530306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56629b96a64d6e6a67bb353c4659a5b6bcbe3d1b5d839623c78e3fbfb5d5d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:f284b77d89a52d6e50f665a70dc9cba7676d350135900856dffad8fa83381129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a60b03d224867bf21b8fcdbedf71f4b988ef38df593113cf167071ae0db1ba`

```dockerfile
```

-	Layers:
	-	`sha256:de6313881469a25f3e98fd3e7a03e6f441046c278766a4991497c229caa95ca8`  
		Last Modified: Thu, 03 Jul 2025 20:07:32 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:1a2b90b79d231f6d79b223f7f6148732566e4f6c8051b02ed9dbb8442cfcd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138128973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7996c20d4b7e0501900c77f11b3517bdde8df963fd95bca52f74102cbee16037`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c35411abd7ff8741d102086e57d13dcf53a36b38d0f83d70dfc564451c476f`  
		Last Modified: Thu, 03 Jul 2025 18:07:38 GMT  
		Size: 9.5 MB (9461151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4334023f752ea84943589c958d76280ad68320a22b65a8b28032bfef145a87`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 90.1 KB (90064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6838b2f15e318a3756e830fe9328c98594e76f559f183a6a2a82f247414e7`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af830fec2f9b00ff6031aa3b5abf77926f1f8ec61c43c2fd933a53aeec3b9716`  
		Last Modified: Thu, 03 Jul 2025 18:07:40 GMT  
		Size: 58.2 MB (58196228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caaa15e0a3e27f74ea0cdc96286507cdae37c6b9da9f6dd58b75262174e04c`  
		Last Modified: Thu, 03 Jul 2025 18:07:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5519b7b6fb48cbf0f06bcb48d96dac6ae50d2f29df217e3ed905c33cfab0f0ff`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:9fbda7207e684fc22b48dcb3d1cb9b90be4e59a79e8f051557e013f5098a80e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f6cfed87f8a2540111bff41a1e80f225970a9299f983f4513c8cb7bc11b3d3`

```dockerfile
```

-	Layers:
	-	`sha256:cefef8bf5e16c3e687c0fa2dec76440f45a5dfecfd26a50caecaeff9ca6c7528`  
		Last Modified: Thu, 03 Jul 2025 20:07:36 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:73e517576082f7d56a5d5d498e3213393339b90ec3f7b5716b77e74da9a7dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136275323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e52499045af79026f3a96eb634a83bcbfcc05f78d5156c2a02d7d17434ed51`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8283e24f943182f28dc30d039850e13d96eafad82bb6c22a140c3efe652058c1`  
		Last Modified: Thu, 03 Jul 2025 18:08:05 GMT  
		Size: 8.6 MB (8610439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450a67de7fa2fbc5711e2fdfa60c7a2945e5a35ffe63f7bc37853d0460923`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 86.5 KB (86500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9b557ed7aa7cbe6b15891cd15a970a5153869d665c096b93ce12aba19709c`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5256c88f5ca619407e171fec8e2327d32bdbb28ff0039389c324c0957d51e2a7`  
		Last Modified: Thu, 03 Jul 2025 18:08:13 GMT  
		Size: 58.2 MB (58196195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5ad95ba8e852e939d06670a567addbe1f7545dfcf9cc2f0bc72df2a549f192`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9ec3f7bf60f8287e8fb6b564e36112f40c678b0a2419e630d97e2eee47d12`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:676399e8815c91e2f684422dcc72561d36f8b71d0a31afa4f8167e54862d165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47da4f2e8332513e7f2fd9f4207d0b2046cb012304e8af3010c40bc64f11e5e8`

```dockerfile
```

-	Layers:
	-	`sha256:e377a69875e60adb621efef5a8aca158b3dafb7230b4f16619be0970236a7d43`  
		Last Modified: Thu, 03 Jul 2025 20:07:39 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9091b93a0497a742433859af71e9d2cbf91a04b4f8b463b2a3ac7bccf626b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138567854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7777fe83512e386382fb92ecdee5fab02657d37d0e4f5c421aa77b3a7e64c3b6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:0a04bc025db0198b912fa1aaba813b1f2e18956dd246940e2a1e7fc2edc56a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b366a219a7150c173e76372f82ae9e34c8c02de7aa62cb30dd1b0d33c196573c`

```dockerfile
```

-	Layers:
	-	`sha256:3650e92878e003d91cb996c90670a5c4fc7f62157f8338da233bf84fee665245`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-cli`

```console
$ docker pull docker@sha256:d623d8d72aa526abcdc996ac8963062a715235ffda58556d864112b8b3fab21b
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

### `docker:28.3-cli` - linux; amd64

```console
$ docker pull docker@sha256:85b2b37853090b68f2bec9b58a28c514aa4a92821231590662d961ec69ca3bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75408319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0884f72ce3334bfac5c84db32abe1dbd7d6d3b0eaeda1735e8e1c5017582741b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6e8ad138fd78450c30c813f8090cdde12769d5d73beb9c3074783e319a24839d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bceb0017eb30fe94b56cfaebf3348fa544b1440eda09cd6afd8a01f4111633`

```dockerfile
```

-	Layers:
	-	`sha256:665d67252df18d6a5da27a11150b2176a16e3ccfa6892683968a9bd2c30e670c`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a3adc3151b74ccad480eee90a0785c6bbf00ae197b29da17912540a9c6307df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70375532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17419babf75f830d0703a82c44c1ea73abe9ad55bc6ecf940e7b6094ace9dff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:26df6789e84e297b20d944fb722165f5a370ea64e3feab5f200814bcebda2025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0fbbe78fe8f5212ac315d751f274fb1730455ffc3833b07d1aeddd8de82656`

```dockerfile
```

-	Layers:
	-	`sha256:1ffa78e1803982dfe37ed32d4c1bd928dfb46888778cd8bf093da83cd5b55b46`  
		Last Modified: Thu, 03 Jul 2025 20:07:47 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c6088237d22ce9f1c74b09f299ffc9f660ae3d9b0b05cf68e70974559ef0b72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69376189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10eeb922114f57e5118d438eef0c96af65407b628eafbe137c8fdb51fcad1d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4620cfbab6b718b6d7608e646d78fee8bd24e4a9e3998c00d2cdb9fc500a4d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0119c9efe61eb4c2a2315fc24b97f0186bdecc9db92ff39c084e27c154054af`

```dockerfile
```

-	Layers:
	-	`sha256:5ab8fb7ac3eb539be8a1207dcaf14c686d92029c58cf5144592f402daaafb75b`  
		Last Modified: Thu, 03 Jul 2025 20:07:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:345329b66e3b117cfabf618ee56c67a4ce9ee4226ed3bf4b2b62d98e8d15e90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7302f18f8f6a2df7421bf64634eb1a82bab0d8397a5cfeed34f49ad79288594d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6972a69e584db7ee5fb8279874ef80ea710672907c48d4e75432ecec12a692bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36eae856160dae536d39b9a3894bcdd53e6a8515faedf00b3ed1d0b03dff1a6`

```dockerfile
```

-	Layers:
	-	`sha256:1202a1d5f73476f0c58ffdbc17ef1175dc800026e4e305fffb0e8a8f847c4234`  
		Last Modified: Thu, 03 Jul 2025 20:07:57 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-dind`

```console
$ docker pull docker@sha256:0a2ee60851e1b61a54707476526c4ed48cc55641a17a5cba8a77fb78e7a4742c
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

### `docker:28.3-dind` - linux; amd64

```console
$ docker pull docker@sha256:af6f4a6f99d3b928aaf2a4c89c92362b61fe5714ce4b359357a7034d72addbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147530306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56629b96a64d6e6a67bb353c4659a5b6bcbe3d1b5d839623c78e3fbfb5d5d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f284b77d89a52d6e50f665a70dc9cba7676d350135900856dffad8fa83381129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a60b03d224867bf21b8fcdbedf71f4b988ef38df593113cf167071ae0db1ba`

```dockerfile
```

-	Layers:
	-	`sha256:de6313881469a25f3e98fd3e7a03e6f441046c278766a4991497c229caa95ca8`  
		Last Modified: Thu, 03 Jul 2025 20:07:32 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1a2b90b79d231f6d79b223f7f6148732566e4f6c8051b02ed9dbb8442cfcd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138128973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7996c20d4b7e0501900c77f11b3517bdde8df963fd95bca52f74102cbee16037`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c35411abd7ff8741d102086e57d13dcf53a36b38d0f83d70dfc564451c476f`  
		Last Modified: Thu, 03 Jul 2025 18:07:38 GMT  
		Size: 9.5 MB (9461151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4334023f752ea84943589c958d76280ad68320a22b65a8b28032bfef145a87`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 90.1 KB (90064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6838b2f15e318a3756e830fe9328c98594e76f559f183a6a2a82f247414e7`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af830fec2f9b00ff6031aa3b5abf77926f1f8ec61c43c2fd933a53aeec3b9716`  
		Last Modified: Thu, 03 Jul 2025 18:07:40 GMT  
		Size: 58.2 MB (58196228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caaa15e0a3e27f74ea0cdc96286507cdae37c6b9da9f6dd58b75262174e04c`  
		Last Modified: Thu, 03 Jul 2025 18:07:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5519b7b6fb48cbf0f06bcb48d96dac6ae50d2f29df217e3ed905c33cfab0f0ff`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9fbda7207e684fc22b48dcb3d1cb9b90be4e59a79e8f051557e013f5098a80e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f6cfed87f8a2540111bff41a1e80f225970a9299f983f4513c8cb7bc11b3d3`

```dockerfile
```

-	Layers:
	-	`sha256:cefef8bf5e16c3e687c0fa2dec76440f45a5dfecfd26a50caecaeff9ca6c7528`  
		Last Modified: Thu, 03 Jul 2025 20:07:36 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:73e517576082f7d56a5d5d498e3213393339b90ec3f7b5716b77e74da9a7dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136275323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e52499045af79026f3a96eb634a83bcbfcc05f78d5156c2a02d7d17434ed51`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8283e24f943182f28dc30d039850e13d96eafad82bb6c22a140c3efe652058c1`  
		Last Modified: Thu, 03 Jul 2025 18:08:05 GMT  
		Size: 8.6 MB (8610439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450a67de7fa2fbc5711e2fdfa60c7a2945e5a35ffe63f7bc37853d0460923`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 86.5 KB (86500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9b557ed7aa7cbe6b15891cd15a970a5153869d665c096b93ce12aba19709c`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5256c88f5ca619407e171fec8e2327d32bdbb28ff0039389c324c0957d51e2a7`  
		Last Modified: Thu, 03 Jul 2025 18:08:13 GMT  
		Size: 58.2 MB (58196195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5ad95ba8e852e939d06670a567addbe1f7545dfcf9cc2f0bc72df2a549f192`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9ec3f7bf60f8287e8fb6b564e36112f40c678b0a2419e630d97e2eee47d12`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:676399e8815c91e2f684422dcc72561d36f8b71d0a31afa4f8167e54862d165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47da4f2e8332513e7f2fd9f4207d0b2046cb012304e8af3010c40bc64f11e5e8`

```dockerfile
```

-	Layers:
	-	`sha256:e377a69875e60adb621efef5a8aca158b3dafb7230b4f16619be0970236a7d43`  
		Last Modified: Thu, 03 Jul 2025 20:07:39 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9091b93a0497a742433859af71e9d2cbf91a04b4f8b463b2a3ac7bccf626b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138567854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7777fe83512e386382fb92ecdee5fab02657d37d0e4f5c421aa77b3a7e64c3b6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0a04bc025db0198b912fa1aaba813b1f2e18956dd246940e2a1e7fc2edc56a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b366a219a7150c173e76372f82ae9e34c8c02de7aa62cb30dd1b0d33c196573c`

```dockerfile
```

-	Layers:
	-	`sha256:3650e92878e003d91cb996c90670a5c4fc7f62157f8338da233bf84fee665245`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-dind-rootless`

```console
$ docker pull docker@sha256:b44749d9b6aba4f5f80bb759bb6ea83e62a1f2c8c0897ad059c5eeafb8d43c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:db4c04bc4465b0434d622bf882950ce45685a378b0ee811e9e1b1219ba6e9436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168515988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21511f843dd54e89f5b101840d8b53c72e1c5ddcd62a5f854485baaa6600fa9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b828347c2a041335957c90cb55b04a323af16f817d2ea2aaa04c38fd9e0a915b`  
		Last Modified: Thu, 03 Jul 2025 18:11:38 GMT  
		Size: 3.4 MB (3398182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9015f88f20407c97d95eec2557adffa39da70fe898e9ef54cc056e91f839250`  
		Last Modified: Thu, 03 Jul 2025 18:11:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fe64c2be9d18d459bedfb0eaae711ac691aae9da049d2259fa61694eebd252`  
		Last Modified: Thu, 03 Jul 2025 18:11:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6974db92eb03859ebac691c35b3b8e4bda756d27667351ec08ad27e3cebb426`  
		Last Modified: Thu, 03 Jul 2025 18:11:40 GMT  
		Size: 17.6 MB (17586158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69244f3e5323c1ad99d83700a10a30cbf3c9b59bd1d6deeb518016c91586411e`  
		Last Modified: Thu, 03 Jul 2025 18:11:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a0cc335b94ca365a19094d5303c10b30b5b1662788b30690d3a98d802427f0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d20f1d9888c19a6d1afdef8729e43aec20f90f322855e9b5c650247836ff0c`

```dockerfile
```

-	Layers:
	-	`sha256:e2532b0be60f5ccad634be0410f2b01c3922c3e42bfc227d2e206c65d2636109`  
		Last Modified: Thu, 03 Jul 2025 20:07:54 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5cedcdbd876edad79f8f62fec3ae650536577aa61a559acaa654dc6f6af631b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159976175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c81ca73fc3e1d219a425a73736a34d915776a8259e79eedd00597f482971cc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055439fa6d8fcc51af0c10bf7bc294b0e1f51845f1fdf975c6f2ed005a72dd7`  
		Last Modified: Thu, 03 Jul 2025 18:22:09 GMT  
		Size: 3.4 MB (3389671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5a4b35eded985f79fbbe8910bab2457acf21a3a5174dc98c50b5a52d6ae94c`  
		Last Modified: Thu, 03 Jul 2025 18:22:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a53aeca772b1453a3107bc47c8fa4c0a699b795f5bb46ce8147903629091105`  
		Last Modified: Thu, 03 Jul 2025 18:22:08 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae30160e013cd77a67fb1c70bca1161363b6d03b329bdbacdb070411f5fab194`  
		Last Modified: Thu, 03 Jul 2025 18:22:10 GMT  
		Size: 18.0 MB (18017309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156b018b4075be77289b3748988b7f34a0e22844508c688dcb3d3fbf47cba9c5`  
		Last Modified: Thu, 03 Jul 2025 18:22:08 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f92dbdaa152a7b0b5985bc9fb607ae59b1f53293d7e03ed0a763bfdb11d65c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e0049363c6bc42c7778de09c867a855ecc9d304eed6f5197c9c0be01a92207`

```dockerfile
```

-	Layers:
	-	`sha256:ddb6058b675b6f844f3eeb5728ee724318dd9b2b36a6a2ac8c90f51f2a3f80a3`  
		Last Modified: Thu, 03 Jul 2025 20:07:57 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-windowsservercore`

```console
$ docker pull docker@sha256:7bc3cbaeffb673a3857fad815ce1bc01a5ffe74778eeb337ad55c118c72f836a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28.3-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:6fd3a0953d971332397c8e5f14fa538fc9feb8ee0df0761ef69cc664d2c15d5a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542412535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7fb045a7559131f0319249930363ace2c34f3549f5254f962c31ec2b021974`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 03 Jul 2025 17:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:28:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:28:01 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:28:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:28:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:28:17 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:28:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:28:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:28:30 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:28:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8360bc4e45fd1207fbb8507f009f2fafe0c692dda8013b87da385b1687fdb93`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee70f98e67bab9d88bef6785da7dcb0243c6678f90f98f1819bb1d6f15bc400`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 401.7 KB (401674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79844d9fe7e509cc013db5713ac75c91fdef2469815feec90b5b5ccad0760d`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6417f363ada4659759175f87056dac7cb772357f80f942c6f12d9c3a511ae2`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754e9768d552528080346d5f1236df2b7fec0cc26703a72181ab5c56597d3874`  
		Last Modified: Thu, 03 Jul 2025 17:32:16 GMT  
		Size: 20.9 MB (20869952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773798f77aa5f53805ec80969f800c997234c80e3eeaeb70915df160d58698d7`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08de61fa1493600c5c1abb22fb424babbd40f76e25bc0cb27af06a1e6826699`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9638f01c3683753b6296eba7747c7453af7e93065c1727c6b1c271fe3a9ad03`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2aa5bce1514c94a539188e90cbf3433418f9aee7b02aa6196d1b252701f4a6`  
		Last Modified: Thu, 03 Jul 2025 17:32:17 GMT  
		Size: 22.7 MB (22693614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b469a4641279b25c6f4c69230acb7f20cf78488659ef25e4b936f65ad62f7f`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94637a4a498775806b5d83e9b9a5dc8b4630e91f61f2560420791e57745cf4ff`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b5885e19d477e90daf5b71748592e75e7b6b7ff7acedc236c6872db6a7e27`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c38a51f4f1af8ed66ca040eb007a92422ee88d91d4dd660bd0f0f5214c46e7c`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 22.3 MB (22261431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.3-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:0dfbb2cb73e0f119f7827c4294818bae9e2b593f4f499366be7ab74496416a06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346334126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2405e622d57138fe3077ec39b9f3f42ebcd0cfdf09f47419ba243ae7fdd5b79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 03 Jul 2025 17:22:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:22:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:22:33 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:22:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:22:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:22:51 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:22:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:22:53 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:23:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:23:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:23:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:23:11 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:23:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b61b501a45983587b82cbf3ec9a02d5dc816be481f91442c358c854092ae35f`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f44a2afa65d60b4bf8e64db5fe87206c5d6caea4df5f91ab8520f7775c6108`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 361.4 KB (361411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a33626ee108dfe569f1ac806973edaad156af082da5adb5cdc619d671c92af`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415464cc927cf6550b8b02ab9a1c7d7076b523ce7f3eb3d6cb06af3cb0717cd`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece6c486f7a91317125ee5a8a9703bd97ad6fe62ffa3eed7300b64d6dae5658c`  
		Last Modified: Thu, 03 Jul 2025 17:23:46 GMT  
		Size: 20.8 MB (20833794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cca4e9c6c6042835085a7bec40bfedfff801d6a5bb1c55fd0d69f3cb4224c5`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e45039c40258e0ad1ddc66ea6789239b16daa6e4b25ad6133a2a0f9155e84e`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d056b131a087efcd1c66a659d7faab0e72b58a72df8d673e794b12df4133e2`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec084cd1ecfecc49f2aee4ece051aaf3b0e26d486dc4f206b8cdca3c459bbba3`  
		Last Modified: Thu, 03 Jul 2025 17:23:44 GMT  
		Size: 22.7 MB (22657606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746d4353372224213706d143dd92b6b6bb55a75ea19c08d8bf0a1831262fae78`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3131944c8f3aa2bfd1c82fa466a67d152080ddf612067169becafb202be3370`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbcaf71c6e95bc4ab5d255abea93afd44db0486b886ce5701bced2305375566`  
		Last Modified: Thu, 03 Jul 2025 17:23:43 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67da6c0deee4b547055907682ae68fc855d99f2e93d43f6e5b6959c0dd55db5e`  
		Last Modified: Thu, 03 Jul 2025 17:23:45 GMT  
		Size: 22.2 MB (22218098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3b16a51f7b350f70417bf9bd061388412d4fe13605c264cd3965ad44c040b98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28.3-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:0dfbb2cb73e0f119f7827c4294818bae9e2b593f4f499366be7ab74496416a06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346334126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2405e622d57138fe3077ec39b9f3f42ebcd0cfdf09f47419ba243ae7fdd5b79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 03 Jul 2025 17:22:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:22:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:22:33 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:22:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:22:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:22:51 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:22:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:22:53 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:23:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:23:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:23:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:23:11 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:23:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b61b501a45983587b82cbf3ec9a02d5dc816be481f91442c358c854092ae35f`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f44a2afa65d60b4bf8e64db5fe87206c5d6caea4df5f91ab8520f7775c6108`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 361.4 KB (361411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a33626ee108dfe569f1ac806973edaad156af082da5adb5cdc619d671c92af`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415464cc927cf6550b8b02ab9a1c7d7076b523ce7f3eb3d6cb06af3cb0717cd`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece6c486f7a91317125ee5a8a9703bd97ad6fe62ffa3eed7300b64d6dae5658c`  
		Last Modified: Thu, 03 Jul 2025 17:23:46 GMT  
		Size: 20.8 MB (20833794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cca4e9c6c6042835085a7bec40bfedfff801d6a5bb1c55fd0d69f3cb4224c5`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e45039c40258e0ad1ddc66ea6789239b16daa6e4b25ad6133a2a0f9155e84e`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d056b131a087efcd1c66a659d7faab0e72b58a72df8d673e794b12df4133e2`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec084cd1ecfecc49f2aee4ece051aaf3b0e26d486dc4f206b8cdca3c459bbba3`  
		Last Modified: Thu, 03 Jul 2025 17:23:44 GMT  
		Size: 22.7 MB (22657606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746d4353372224213706d143dd92b6b6bb55a75ea19c08d8bf0a1831262fae78`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3131944c8f3aa2bfd1c82fa466a67d152080ddf612067169becafb202be3370`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbcaf71c6e95bc4ab5d255abea93afd44db0486b886ce5701bced2305375566`  
		Last Modified: Thu, 03 Jul 2025 17:23:43 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67da6c0deee4b547055907682ae68fc855d99f2e93d43f6e5b6959c0dd55db5e`  
		Last Modified: Thu, 03 Jul 2025 17:23:45 GMT  
		Size: 22.2 MB (22218098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:47e4025f5f5eb4bb57f9bc7b3c77d306050988fe620d7ee3e7af4720382fe323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28.3-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:6fd3a0953d971332397c8e5f14fa538fc9feb8ee0df0761ef69cc664d2c15d5a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542412535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7fb045a7559131f0319249930363ace2c34f3549f5254f962c31ec2b021974`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 03 Jul 2025 17:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:28:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:28:01 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:28:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:28:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:28:17 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:28:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:28:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:28:30 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:28:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8360bc4e45fd1207fbb8507f009f2fafe0c692dda8013b87da385b1687fdb93`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee70f98e67bab9d88bef6785da7dcb0243c6678f90f98f1819bb1d6f15bc400`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 401.7 KB (401674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79844d9fe7e509cc013db5713ac75c91fdef2469815feec90b5b5ccad0760d`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6417f363ada4659759175f87056dac7cb772357f80f942c6f12d9c3a511ae2`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754e9768d552528080346d5f1236df2b7fec0cc26703a72181ab5c56597d3874`  
		Last Modified: Thu, 03 Jul 2025 17:32:16 GMT  
		Size: 20.9 MB (20869952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773798f77aa5f53805ec80969f800c997234c80e3eeaeb70915df160d58698d7`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08de61fa1493600c5c1abb22fb424babbd40f76e25bc0cb27af06a1e6826699`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9638f01c3683753b6296eba7747c7453af7e93065c1727c6b1c271fe3a9ad03`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2aa5bce1514c94a539188e90cbf3433418f9aee7b02aa6196d1b252701f4a6`  
		Last Modified: Thu, 03 Jul 2025 17:32:17 GMT  
		Size: 22.7 MB (22693614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b469a4641279b25c6f4c69230acb7f20cf78488659ef25e4b936f65ad62f7f`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94637a4a498775806b5d83e9b9a5dc8b4630e91f61f2560420791e57745cf4ff`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b5885e19d477e90daf5b71748592e75e7b6b7ff7acedc236c6872db6a7e27`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c38a51f4f1af8ed66ca040eb007a92422ee88d91d4dd660bd0f0f5214c46e7c`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 22.3 MB (22261431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.1`

```console
$ docker pull docker@sha256:0a2ee60851e1b61a54707476526c4ed48cc55641a17a5cba8a77fb78e7a4742c
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

### `docker:28.3.1` - linux; amd64

```console
$ docker pull docker@sha256:af6f4a6f99d3b928aaf2a4c89c92362b61fe5714ce4b359357a7034d72addbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147530306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56629b96a64d6e6a67bb353c4659a5b6bcbe3d1b5d839623c78e3fbfb5d5d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:f284b77d89a52d6e50f665a70dc9cba7676d350135900856dffad8fa83381129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a60b03d224867bf21b8fcdbedf71f4b988ef38df593113cf167071ae0db1ba`

```dockerfile
```

-	Layers:
	-	`sha256:de6313881469a25f3e98fd3e7a03e6f441046c278766a4991497c229caa95ca8`  
		Last Modified: Thu, 03 Jul 2025 20:07:32 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:1a2b90b79d231f6d79b223f7f6148732566e4f6c8051b02ed9dbb8442cfcd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138128973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7996c20d4b7e0501900c77f11b3517bdde8df963fd95bca52f74102cbee16037`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c35411abd7ff8741d102086e57d13dcf53a36b38d0f83d70dfc564451c476f`  
		Last Modified: Thu, 03 Jul 2025 18:07:38 GMT  
		Size: 9.5 MB (9461151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4334023f752ea84943589c958d76280ad68320a22b65a8b28032bfef145a87`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 90.1 KB (90064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6838b2f15e318a3756e830fe9328c98594e76f559f183a6a2a82f247414e7`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af830fec2f9b00ff6031aa3b5abf77926f1f8ec61c43c2fd933a53aeec3b9716`  
		Last Modified: Thu, 03 Jul 2025 18:07:40 GMT  
		Size: 58.2 MB (58196228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caaa15e0a3e27f74ea0cdc96286507cdae37c6b9da9f6dd58b75262174e04c`  
		Last Modified: Thu, 03 Jul 2025 18:07:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5519b7b6fb48cbf0f06bcb48d96dac6ae50d2f29df217e3ed905c33cfab0f0ff`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:9fbda7207e684fc22b48dcb3d1cb9b90be4e59a79e8f051557e013f5098a80e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f6cfed87f8a2540111bff41a1e80f225970a9299f983f4513c8cb7bc11b3d3`

```dockerfile
```

-	Layers:
	-	`sha256:cefef8bf5e16c3e687c0fa2dec76440f45a5dfecfd26a50caecaeff9ca6c7528`  
		Last Modified: Thu, 03 Jul 2025 20:07:36 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:73e517576082f7d56a5d5d498e3213393339b90ec3f7b5716b77e74da9a7dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136275323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e52499045af79026f3a96eb634a83bcbfcc05f78d5156c2a02d7d17434ed51`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8283e24f943182f28dc30d039850e13d96eafad82bb6c22a140c3efe652058c1`  
		Last Modified: Thu, 03 Jul 2025 18:08:05 GMT  
		Size: 8.6 MB (8610439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450a67de7fa2fbc5711e2fdfa60c7a2945e5a35ffe63f7bc37853d0460923`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 86.5 KB (86500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9b557ed7aa7cbe6b15891cd15a970a5153869d665c096b93ce12aba19709c`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5256c88f5ca619407e171fec8e2327d32bdbb28ff0039389c324c0957d51e2a7`  
		Last Modified: Thu, 03 Jul 2025 18:08:13 GMT  
		Size: 58.2 MB (58196195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5ad95ba8e852e939d06670a567addbe1f7545dfcf9cc2f0bc72df2a549f192`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9ec3f7bf60f8287e8fb6b564e36112f40c678b0a2419e630d97e2eee47d12`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:676399e8815c91e2f684422dcc72561d36f8b71d0a31afa4f8167e54862d165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47da4f2e8332513e7f2fd9f4207d0b2046cb012304e8af3010c40bc64f11e5e8`

```dockerfile
```

-	Layers:
	-	`sha256:e377a69875e60adb621efef5a8aca158b3dafb7230b4f16619be0970236a7d43`  
		Last Modified: Thu, 03 Jul 2025 20:07:39 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9091b93a0497a742433859af71e9d2cbf91a04b4f8b463b2a3ac7bccf626b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138567854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7777fe83512e386382fb92ecdee5fab02657d37d0e4f5c421aa77b3a7e64c3b6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:0a04bc025db0198b912fa1aaba813b1f2e18956dd246940e2a1e7fc2edc56a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b366a219a7150c173e76372f82ae9e34c8c02de7aa62cb30dd1b0d33c196573c`

```dockerfile
```

-	Layers:
	-	`sha256:3650e92878e003d91cb996c90670a5c4fc7f62157f8338da233bf84fee665245`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.1-alpine3.22`

```console
$ docker pull docker@sha256:0a2ee60851e1b61a54707476526c4ed48cc55641a17a5cba8a77fb78e7a4742c
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

### `docker:28.3.1-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:af6f4a6f99d3b928aaf2a4c89c92362b61fe5714ce4b359357a7034d72addbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147530306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56629b96a64d6e6a67bb353c4659a5b6bcbe3d1b5d839623c78e3fbfb5d5d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f284b77d89a52d6e50f665a70dc9cba7676d350135900856dffad8fa83381129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a60b03d224867bf21b8fcdbedf71f4b988ef38df593113cf167071ae0db1ba`

```dockerfile
```

-	Layers:
	-	`sha256:de6313881469a25f3e98fd3e7a03e6f441046c278766a4991497c229caa95ca8`  
		Last Modified: Thu, 03 Jul 2025 20:07:32 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:1a2b90b79d231f6d79b223f7f6148732566e4f6c8051b02ed9dbb8442cfcd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138128973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7996c20d4b7e0501900c77f11b3517bdde8df963fd95bca52f74102cbee16037`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c35411abd7ff8741d102086e57d13dcf53a36b38d0f83d70dfc564451c476f`  
		Last Modified: Thu, 03 Jul 2025 18:07:38 GMT  
		Size: 9.5 MB (9461151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4334023f752ea84943589c958d76280ad68320a22b65a8b28032bfef145a87`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 90.1 KB (90064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6838b2f15e318a3756e830fe9328c98594e76f559f183a6a2a82f247414e7`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af830fec2f9b00ff6031aa3b5abf77926f1f8ec61c43c2fd933a53aeec3b9716`  
		Last Modified: Thu, 03 Jul 2025 18:07:40 GMT  
		Size: 58.2 MB (58196228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caaa15e0a3e27f74ea0cdc96286507cdae37c6b9da9f6dd58b75262174e04c`  
		Last Modified: Thu, 03 Jul 2025 18:07:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5519b7b6fb48cbf0f06bcb48d96dac6ae50d2f29df217e3ed905c33cfab0f0ff`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:9fbda7207e684fc22b48dcb3d1cb9b90be4e59a79e8f051557e013f5098a80e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f6cfed87f8a2540111bff41a1e80f225970a9299f983f4513c8cb7bc11b3d3`

```dockerfile
```

-	Layers:
	-	`sha256:cefef8bf5e16c3e687c0fa2dec76440f45a5dfecfd26a50caecaeff9ca6c7528`  
		Last Modified: Thu, 03 Jul 2025 20:07:36 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:73e517576082f7d56a5d5d498e3213393339b90ec3f7b5716b77e74da9a7dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136275323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e52499045af79026f3a96eb634a83bcbfcc05f78d5156c2a02d7d17434ed51`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8283e24f943182f28dc30d039850e13d96eafad82bb6c22a140c3efe652058c1`  
		Last Modified: Thu, 03 Jul 2025 18:08:05 GMT  
		Size: 8.6 MB (8610439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450a67de7fa2fbc5711e2fdfa60c7a2945e5a35ffe63f7bc37853d0460923`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 86.5 KB (86500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9b557ed7aa7cbe6b15891cd15a970a5153869d665c096b93ce12aba19709c`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5256c88f5ca619407e171fec8e2327d32bdbb28ff0039389c324c0957d51e2a7`  
		Last Modified: Thu, 03 Jul 2025 18:08:13 GMT  
		Size: 58.2 MB (58196195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5ad95ba8e852e939d06670a567addbe1f7545dfcf9cc2f0bc72df2a549f192`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9ec3f7bf60f8287e8fb6b564e36112f40c678b0a2419e630d97e2eee47d12`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:676399e8815c91e2f684422dcc72561d36f8b71d0a31afa4f8167e54862d165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47da4f2e8332513e7f2fd9f4207d0b2046cb012304e8af3010c40bc64f11e5e8`

```dockerfile
```

-	Layers:
	-	`sha256:e377a69875e60adb621efef5a8aca158b3dafb7230b4f16619be0970236a7d43`  
		Last Modified: Thu, 03 Jul 2025 20:07:39 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9091b93a0497a742433859af71e9d2cbf91a04b4f8b463b2a3ac7bccf626b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138567854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7777fe83512e386382fb92ecdee5fab02657d37d0e4f5c421aa77b3a7e64c3b6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:0a04bc025db0198b912fa1aaba813b1f2e18956dd246940e2a1e7fc2edc56a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b366a219a7150c173e76372f82ae9e34c8c02de7aa62cb30dd1b0d33c196573c`

```dockerfile
```

-	Layers:
	-	`sha256:3650e92878e003d91cb996c90670a5c4fc7f62157f8338da233bf84fee665245`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.1-cli`

```console
$ docker pull docker@sha256:d623d8d72aa526abcdc996ac8963062a715235ffda58556d864112b8b3fab21b
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

### `docker:28.3.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:85b2b37853090b68f2bec9b58a28c514aa4a92821231590662d961ec69ca3bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75408319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0884f72ce3334bfac5c84db32abe1dbd7d6d3b0eaeda1735e8e1c5017582741b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6e8ad138fd78450c30c813f8090cdde12769d5d73beb9c3074783e319a24839d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bceb0017eb30fe94b56cfaebf3348fa544b1440eda09cd6afd8a01f4111633`

```dockerfile
```

-	Layers:
	-	`sha256:665d67252df18d6a5da27a11150b2176a16e3ccfa6892683968a9bd2c30e670c`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a3adc3151b74ccad480eee90a0785c6bbf00ae197b29da17912540a9c6307df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70375532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17419babf75f830d0703a82c44c1ea73abe9ad55bc6ecf940e7b6094ace9dff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:26df6789e84e297b20d944fb722165f5a370ea64e3feab5f200814bcebda2025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0fbbe78fe8f5212ac315d751f274fb1730455ffc3833b07d1aeddd8de82656`

```dockerfile
```

-	Layers:
	-	`sha256:1ffa78e1803982dfe37ed32d4c1bd928dfb46888778cd8bf093da83cd5b55b46`  
		Last Modified: Thu, 03 Jul 2025 20:07:47 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c6088237d22ce9f1c74b09f299ffc9f660ae3d9b0b05cf68e70974559ef0b72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69376189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10eeb922114f57e5118d438eef0c96af65407b628eafbe137c8fdb51fcad1d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4620cfbab6b718b6d7608e646d78fee8bd24e4a9e3998c00d2cdb9fc500a4d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0119c9efe61eb4c2a2315fc24b97f0186bdecc9db92ff39c084e27c154054af`

```dockerfile
```

-	Layers:
	-	`sha256:5ab8fb7ac3eb539be8a1207dcaf14c686d92029c58cf5144592f402daaafb75b`  
		Last Modified: Thu, 03 Jul 2025 20:07:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:345329b66e3b117cfabf618ee56c67a4ce9ee4226ed3bf4b2b62d98e8d15e90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7302f18f8f6a2df7421bf64634eb1a82bab0d8397a5cfeed34f49ad79288594d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6972a69e584db7ee5fb8279874ef80ea710672907c48d4e75432ecec12a692bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36eae856160dae536d39b9a3894bcdd53e6a8515faedf00b3ed1d0b03dff1a6`

```dockerfile
```

-	Layers:
	-	`sha256:1202a1d5f73476f0c58ffdbc17ef1175dc800026e4e305fffb0e8a8f847c4234`  
		Last Modified: Thu, 03 Jul 2025 20:07:57 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.1-cli-alpine3.22`

```console
$ docker pull docker@sha256:d623d8d72aa526abcdc996ac8963062a715235ffda58556d864112b8b3fab21b
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

### `docker:28.3.1-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:85b2b37853090b68f2bec9b58a28c514aa4a92821231590662d961ec69ca3bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75408319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0884f72ce3334bfac5c84db32abe1dbd7d6d3b0eaeda1735e8e1c5017582741b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6e8ad138fd78450c30c813f8090cdde12769d5d73beb9c3074783e319a24839d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bceb0017eb30fe94b56cfaebf3348fa544b1440eda09cd6afd8a01f4111633`

```dockerfile
```

-	Layers:
	-	`sha256:665d67252df18d6a5da27a11150b2176a16e3ccfa6892683968a9bd2c30e670c`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a3adc3151b74ccad480eee90a0785c6bbf00ae197b29da17912540a9c6307df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70375532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17419babf75f830d0703a82c44c1ea73abe9ad55bc6ecf940e7b6094ace9dff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:26df6789e84e297b20d944fb722165f5a370ea64e3feab5f200814bcebda2025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0fbbe78fe8f5212ac315d751f274fb1730455ffc3833b07d1aeddd8de82656`

```dockerfile
```

-	Layers:
	-	`sha256:1ffa78e1803982dfe37ed32d4c1bd928dfb46888778cd8bf093da83cd5b55b46`  
		Last Modified: Thu, 03 Jul 2025 20:07:47 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:c6088237d22ce9f1c74b09f299ffc9f660ae3d9b0b05cf68e70974559ef0b72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69376189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10eeb922114f57e5118d438eef0c96af65407b628eafbe137c8fdb51fcad1d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:4620cfbab6b718b6d7608e646d78fee8bd24e4a9e3998c00d2cdb9fc500a4d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0119c9efe61eb4c2a2315fc24b97f0186bdecc9db92ff39c084e27c154054af`

```dockerfile
```

-	Layers:
	-	`sha256:5ab8fb7ac3eb539be8a1207dcaf14c686d92029c58cf5144592f402daaafb75b`  
		Last Modified: Thu, 03 Jul 2025 20:07:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:345329b66e3b117cfabf618ee56c67a4ce9ee4226ed3bf4b2b62d98e8d15e90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7302f18f8f6a2df7421bf64634eb1a82bab0d8397a5cfeed34f49ad79288594d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6972a69e584db7ee5fb8279874ef80ea710672907c48d4e75432ecec12a692bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36eae856160dae536d39b9a3894bcdd53e6a8515faedf00b3ed1d0b03dff1a6`

```dockerfile
```

-	Layers:
	-	`sha256:1202a1d5f73476f0c58ffdbc17ef1175dc800026e4e305fffb0e8a8f847c4234`  
		Last Modified: Thu, 03 Jul 2025 20:07:57 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.1-dind`

```console
$ docker pull docker@sha256:0a2ee60851e1b61a54707476526c4ed48cc55641a17a5cba8a77fb78e7a4742c
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

### `docker:28.3.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:af6f4a6f99d3b928aaf2a4c89c92362b61fe5714ce4b359357a7034d72addbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147530306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56629b96a64d6e6a67bb353c4659a5b6bcbe3d1b5d839623c78e3fbfb5d5d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f284b77d89a52d6e50f665a70dc9cba7676d350135900856dffad8fa83381129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a60b03d224867bf21b8fcdbedf71f4b988ef38df593113cf167071ae0db1ba`

```dockerfile
```

-	Layers:
	-	`sha256:de6313881469a25f3e98fd3e7a03e6f441046c278766a4991497c229caa95ca8`  
		Last Modified: Thu, 03 Jul 2025 20:07:32 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1a2b90b79d231f6d79b223f7f6148732566e4f6c8051b02ed9dbb8442cfcd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138128973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7996c20d4b7e0501900c77f11b3517bdde8df963fd95bca52f74102cbee16037`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c35411abd7ff8741d102086e57d13dcf53a36b38d0f83d70dfc564451c476f`  
		Last Modified: Thu, 03 Jul 2025 18:07:38 GMT  
		Size: 9.5 MB (9461151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4334023f752ea84943589c958d76280ad68320a22b65a8b28032bfef145a87`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 90.1 KB (90064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6838b2f15e318a3756e830fe9328c98594e76f559f183a6a2a82f247414e7`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af830fec2f9b00ff6031aa3b5abf77926f1f8ec61c43c2fd933a53aeec3b9716`  
		Last Modified: Thu, 03 Jul 2025 18:07:40 GMT  
		Size: 58.2 MB (58196228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caaa15e0a3e27f74ea0cdc96286507cdae37c6b9da9f6dd58b75262174e04c`  
		Last Modified: Thu, 03 Jul 2025 18:07:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5519b7b6fb48cbf0f06bcb48d96dac6ae50d2f29df217e3ed905c33cfab0f0ff`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9fbda7207e684fc22b48dcb3d1cb9b90be4e59a79e8f051557e013f5098a80e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f6cfed87f8a2540111bff41a1e80f225970a9299f983f4513c8cb7bc11b3d3`

```dockerfile
```

-	Layers:
	-	`sha256:cefef8bf5e16c3e687c0fa2dec76440f45a5dfecfd26a50caecaeff9ca6c7528`  
		Last Modified: Thu, 03 Jul 2025 20:07:36 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:73e517576082f7d56a5d5d498e3213393339b90ec3f7b5716b77e74da9a7dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136275323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e52499045af79026f3a96eb634a83bcbfcc05f78d5156c2a02d7d17434ed51`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8283e24f943182f28dc30d039850e13d96eafad82bb6c22a140c3efe652058c1`  
		Last Modified: Thu, 03 Jul 2025 18:08:05 GMT  
		Size: 8.6 MB (8610439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450a67de7fa2fbc5711e2fdfa60c7a2945e5a35ffe63f7bc37853d0460923`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 86.5 KB (86500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9b557ed7aa7cbe6b15891cd15a970a5153869d665c096b93ce12aba19709c`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5256c88f5ca619407e171fec8e2327d32bdbb28ff0039389c324c0957d51e2a7`  
		Last Modified: Thu, 03 Jul 2025 18:08:13 GMT  
		Size: 58.2 MB (58196195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5ad95ba8e852e939d06670a567addbe1f7545dfcf9cc2f0bc72df2a549f192`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9ec3f7bf60f8287e8fb6b564e36112f40c678b0a2419e630d97e2eee47d12`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:676399e8815c91e2f684422dcc72561d36f8b71d0a31afa4f8167e54862d165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47da4f2e8332513e7f2fd9f4207d0b2046cb012304e8af3010c40bc64f11e5e8`

```dockerfile
```

-	Layers:
	-	`sha256:e377a69875e60adb621efef5a8aca158b3dafb7230b4f16619be0970236a7d43`  
		Last Modified: Thu, 03 Jul 2025 20:07:39 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9091b93a0497a742433859af71e9d2cbf91a04b4f8b463b2a3ac7bccf626b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138567854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7777fe83512e386382fb92ecdee5fab02657d37d0e4f5c421aa77b3a7e64c3b6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0a04bc025db0198b912fa1aaba813b1f2e18956dd246940e2a1e7fc2edc56a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b366a219a7150c173e76372f82ae9e34c8c02de7aa62cb30dd1b0d33c196573c`

```dockerfile
```

-	Layers:
	-	`sha256:3650e92878e003d91cb996c90670a5c4fc7f62157f8338da233bf84fee665245`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.1-dind-alpine3.22`

```console
$ docker pull docker@sha256:0a2ee60851e1b61a54707476526c4ed48cc55641a17a5cba8a77fb78e7a4742c
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

### `docker:28.3.1-dind-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:af6f4a6f99d3b928aaf2a4c89c92362b61fe5714ce4b359357a7034d72addbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147530306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56629b96a64d6e6a67bb353c4659a5b6bcbe3d1b5d839623c78e3fbfb5d5d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f284b77d89a52d6e50f665a70dc9cba7676d350135900856dffad8fa83381129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a60b03d224867bf21b8fcdbedf71f4b988ef38df593113cf167071ae0db1ba`

```dockerfile
```

-	Layers:
	-	`sha256:de6313881469a25f3e98fd3e7a03e6f441046c278766a4991497c229caa95ca8`  
		Last Modified: Thu, 03 Jul 2025 20:07:32 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-dind-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:1a2b90b79d231f6d79b223f7f6148732566e4f6c8051b02ed9dbb8442cfcd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138128973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7996c20d4b7e0501900c77f11b3517bdde8df963fd95bca52f74102cbee16037`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c35411abd7ff8741d102086e57d13dcf53a36b38d0f83d70dfc564451c476f`  
		Last Modified: Thu, 03 Jul 2025 18:07:38 GMT  
		Size: 9.5 MB (9461151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4334023f752ea84943589c958d76280ad68320a22b65a8b28032bfef145a87`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 90.1 KB (90064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6838b2f15e318a3756e830fe9328c98594e76f559f183a6a2a82f247414e7`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af830fec2f9b00ff6031aa3b5abf77926f1f8ec61c43c2fd933a53aeec3b9716`  
		Last Modified: Thu, 03 Jul 2025 18:07:40 GMT  
		Size: 58.2 MB (58196228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caaa15e0a3e27f74ea0cdc96286507cdae37c6b9da9f6dd58b75262174e04c`  
		Last Modified: Thu, 03 Jul 2025 18:07:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5519b7b6fb48cbf0f06bcb48d96dac6ae50d2f29df217e3ed905c33cfab0f0ff`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:9fbda7207e684fc22b48dcb3d1cb9b90be4e59a79e8f051557e013f5098a80e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f6cfed87f8a2540111bff41a1e80f225970a9299f983f4513c8cb7bc11b3d3`

```dockerfile
```

-	Layers:
	-	`sha256:cefef8bf5e16c3e687c0fa2dec76440f45a5dfecfd26a50caecaeff9ca6c7528`  
		Last Modified: Thu, 03 Jul 2025 20:07:36 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-dind-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:73e517576082f7d56a5d5d498e3213393339b90ec3f7b5716b77e74da9a7dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136275323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e52499045af79026f3a96eb634a83bcbfcc05f78d5156c2a02d7d17434ed51`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8283e24f943182f28dc30d039850e13d96eafad82bb6c22a140c3efe652058c1`  
		Last Modified: Thu, 03 Jul 2025 18:08:05 GMT  
		Size: 8.6 MB (8610439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450a67de7fa2fbc5711e2fdfa60c7a2945e5a35ffe63f7bc37853d0460923`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 86.5 KB (86500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9b557ed7aa7cbe6b15891cd15a970a5153869d665c096b93ce12aba19709c`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5256c88f5ca619407e171fec8e2327d32bdbb28ff0039389c324c0957d51e2a7`  
		Last Modified: Thu, 03 Jul 2025 18:08:13 GMT  
		Size: 58.2 MB (58196195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5ad95ba8e852e939d06670a567addbe1f7545dfcf9cc2f0bc72df2a549f192`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9ec3f7bf60f8287e8fb6b564e36112f40c678b0a2419e630d97e2eee47d12`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:676399e8815c91e2f684422dcc72561d36f8b71d0a31afa4f8167e54862d165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47da4f2e8332513e7f2fd9f4207d0b2046cb012304e8af3010c40bc64f11e5e8`

```dockerfile
```

-	Layers:
	-	`sha256:e377a69875e60adb621efef5a8aca158b3dafb7230b4f16619be0970236a7d43`  
		Last Modified: Thu, 03 Jul 2025 20:07:39 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-dind-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9091b93a0497a742433859af71e9d2cbf91a04b4f8b463b2a3ac7bccf626b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138567854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7777fe83512e386382fb92ecdee5fab02657d37d0e4f5c421aa77b3a7e64c3b6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:0a04bc025db0198b912fa1aaba813b1f2e18956dd246940e2a1e7fc2edc56a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b366a219a7150c173e76372f82ae9e34c8c02de7aa62cb30dd1b0d33c196573c`

```dockerfile
```

-	Layers:
	-	`sha256:3650e92878e003d91cb996c90670a5c4fc7f62157f8338da233bf84fee665245`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.1-dind-rootless`

```console
$ docker pull docker@sha256:b44749d9b6aba4f5f80bb759bb6ea83e62a1f2c8c0897ad059c5eeafb8d43c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.3.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:db4c04bc4465b0434d622bf882950ce45685a378b0ee811e9e1b1219ba6e9436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168515988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21511f843dd54e89f5b101840d8b53c72e1c5ddcd62a5f854485baaa6600fa9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b828347c2a041335957c90cb55b04a323af16f817d2ea2aaa04c38fd9e0a915b`  
		Last Modified: Thu, 03 Jul 2025 18:11:38 GMT  
		Size: 3.4 MB (3398182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9015f88f20407c97d95eec2557adffa39da70fe898e9ef54cc056e91f839250`  
		Last Modified: Thu, 03 Jul 2025 18:11:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fe64c2be9d18d459bedfb0eaae711ac691aae9da049d2259fa61694eebd252`  
		Last Modified: Thu, 03 Jul 2025 18:11:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6974db92eb03859ebac691c35b3b8e4bda756d27667351ec08ad27e3cebb426`  
		Last Modified: Thu, 03 Jul 2025 18:11:40 GMT  
		Size: 17.6 MB (17586158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69244f3e5323c1ad99d83700a10a30cbf3c9b59bd1d6deeb518016c91586411e`  
		Last Modified: Thu, 03 Jul 2025 18:11:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a0cc335b94ca365a19094d5303c10b30b5b1662788b30690d3a98d802427f0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d20f1d9888c19a6d1afdef8729e43aec20f90f322855e9b5c650247836ff0c`

```dockerfile
```

-	Layers:
	-	`sha256:e2532b0be60f5ccad634be0410f2b01c3922c3e42bfc227d2e206c65d2636109`  
		Last Modified: Thu, 03 Jul 2025 20:07:54 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5cedcdbd876edad79f8f62fec3ae650536577aa61a559acaa654dc6f6af631b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159976175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c81ca73fc3e1d219a425a73736a34d915776a8259e79eedd00597f482971cc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055439fa6d8fcc51af0c10bf7bc294b0e1f51845f1fdf975c6f2ed005a72dd7`  
		Last Modified: Thu, 03 Jul 2025 18:22:09 GMT  
		Size: 3.4 MB (3389671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5a4b35eded985f79fbbe8910bab2457acf21a3a5174dc98c50b5a52d6ae94c`  
		Last Modified: Thu, 03 Jul 2025 18:22:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a53aeca772b1453a3107bc47c8fa4c0a699b795f5bb46ce8147903629091105`  
		Last Modified: Thu, 03 Jul 2025 18:22:08 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae30160e013cd77a67fb1c70bca1161363b6d03b329bdbacdb070411f5fab194`  
		Last Modified: Thu, 03 Jul 2025 18:22:10 GMT  
		Size: 18.0 MB (18017309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156b018b4075be77289b3748988b7f34a0e22844508c688dcb3d3fbf47cba9c5`  
		Last Modified: Thu, 03 Jul 2025 18:22:08 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f92dbdaa152a7b0b5985bc9fb607ae59b1f53293d7e03ed0a763bfdb11d65c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e0049363c6bc42c7778de09c867a855ecc9d304eed6f5197c9c0be01a92207`

```dockerfile
```

-	Layers:
	-	`sha256:ddb6058b675b6f844f3eeb5728ee724318dd9b2b36a6a2ac8c90f51f2a3f80a3`  
		Last Modified: Thu, 03 Jul 2025 20:07:57 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.1-windowsservercore`

```console
$ docker pull docker@sha256:7bc3cbaeffb673a3857fad815ce1bc01a5ffe74778eeb337ad55c118c72f836a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28.3.1-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:6fd3a0953d971332397c8e5f14fa538fc9feb8ee0df0761ef69cc664d2c15d5a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542412535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7fb045a7559131f0319249930363ace2c34f3549f5254f962c31ec2b021974`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 03 Jul 2025 17:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:28:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:28:01 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:28:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:28:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:28:17 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:28:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:28:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:28:30 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:28:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8360bc4e45fd1207fbb8507f009f2fafe0c692dda8013b87da385b1687fdb93`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee70f98e67bab9d88bef6785da7dcb0243c6678f90f98f1819bb1d6f15bc400`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 401.7 KB (401674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79844d9fe7e509cc013db5713ac75c91fdef2469815feec90b5b5ccad0760d`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6417f363ada4659759175f87056dac7cb772357f80f942c6f12d9c3a511ae2`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754e9768d552528080346d5f1236df2b7fec0cc26703a72181ab5c56597d3874`  
		Last Modified: Thu, 03 Jul 2025 17:32:16 GMT  
		Size: 20.9 MB (20869952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773798f77aa5f53805ec80969f800c997234c80e3eeaeb70915df160d58698d7`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08de61fa1493600c5c1abb22fb424babbd40f76e25bc0cb27af06a1e6826699`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9638f01c3683753b6296eba7747c7453af7e93065c1727c6b1c271fe3a9ad03`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2aa5bce1514c94a539188e90cbf3433418f9aee7b02aa6196d1b252701f4a6`  
		Last Modified: Thu, 03 Jul 2025 17:32:17 GMT  
		Size: 22.7 MB (22693614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b469a4641279b25c6f4c69230acb7f20cf78488659ef25e4b936f65ad62f7f`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94637a4a498775806b5d83e9b9a5dc8b4630e91f61f2560420791e57745cf4ff`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b5885e19d477e90daf5b71748592e75e7b6b7ff7acedc236c6872db6a7e27`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c38a51f4f1af8ed66ca040eb007a92422ee88d91d4dd660bd0f0f5214c46e7c`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 22.3 MB (22261431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.3.1-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:0dfbb2cb73e0f119f7827c4294818bae9e2b593f4f499366be7ab74496416a06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346334126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2405e622d57138fe3077ec39b9f3f42ebcd0cfdf09f47419ba243ae7fdd5b79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 03 Jul 2025 17:22:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:22:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:22:33 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:22:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:22:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:22:51 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:22:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:22:53 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:23:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:23:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:23:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:23:11 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:23:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b61b501a45983587b82cbf3ec9a02d5dc816be481f91442c358c854092ae35f`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f44a2afa65d60b4bf8e64db5fe87206c5d6caea4df5f91ab8520f7775c6108`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 361.4 KB (361411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a33626ee108dfe569f1ac806973edaad156af082da5adb5cdc619d671c92af`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415464cc927cf6550b8b02ab9a1c7d7076b523ce7f3eb3d6cb06af3cb0717cd`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece6c486f7a91317125ee5a8a9703bd97ad6fe62ffa3eed7300b64d6dae5658c`  
		Last Modified: Thu, 03 Jul 2025 17:23:46 GMT  
		Size: 20.8 MB (20833794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cca4e9c6c6042835085a7bec40bfedfff801d6a5bb1c55fd0d69f3cb4224c5`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e45039c40258e0ad1ddc66ea6789239b16daa6e4b25ad6133a2a0f9155e84e`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d056b131a087efcd1c66a659d7faab0e72b58a72df8d673e794b12df4133e2`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec084cd1ecfecc49f2aee4ece051aaf3b0e26d486dc4f206b8cdca3c459bbba3`  
		Last Modified: Thu, 03 Jul 2025 17:23:44 GMT  
		Size: 22.7 MB (22657606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746d4353372224213706d143dd92b6b6bb55a75ea19c08d8bf0a1831262fae78`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3131944c8f3aa2bfd1c82fa466a67d152080ddf612067169becafb202be3370`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbcaf71c6e95bc4ab5d255abea93afd44db0486b886ce5701bced2305375566`  
		Last Modified: Thu, 03 Jul 2025 17:23:43 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67da6c0deee4b547055907682ae68fc855d99f2e93d43f6e5b6959c0dd55db5e`  
		Last Modified: Thu, 03 Jul 2025 17:23:45 GMT  
		Size: 22.2 MB (22218098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3b16a51f7b350f70417bf9bd061388412d4fe13605c264cd3965ad44c040b98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28.3.1-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:0dfbb2cb73e0f119f7827c4294818bae9e2b593f4f499366be7ab74496416a06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346334126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2405e622d57138fe3077ec39b9f3f42ebcd0cfdf09f47419ba243ae7fdd5b79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 03 Jul 2025 17:22:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:22:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:22:33 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:22:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:22:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:22:51 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:22:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:22:53 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:23:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:23:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:23:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:23:11 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:23:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b61b501a45983587b82cbf3ec9a02d5dc816be481f91442c358c854092ae35f`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f44a2afa65d60b4bf8e64db5fe87206c5d6caea4df5f91ab8520f7775c6108`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 361.4 KB (361411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a33626ee108dfe569f1ac806973edaad156af082da5adb5cdc619d671c92af`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415464cc927cf6550b8b02ab9a1c7d7076b523ce7f3eb3d6cb06af3cb0717cd`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece6c486f7a91317125ee5a8a9703bd97ad6fe62ffa3eed7300b64d6dae5658c`  
		Last Modified: Thu, 03 Jul 2025 17:23:46 GMT  
		Size: 20.8 MB (20833794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cca4e9c6c6042835085a7bec40bfedfff801d6a5bb1c55fd0d69f3cb4224c5`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e45039c40258e0ad1ddc66ea6789239b16daa6e4b25ad6133a2a0f9155e84e`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d056b131a087efcd1c66a659d7faab0e72b58a72df8d673e794b12df4133e2`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec084cd1ecfecc49f2aee4ece051aaf3b0e26d486dc4f206b8cdca3c459bbba3`  
		Last Modified: Thu, 03 Jul 2025 17:23:44 GMT  
		Size: 22.7 MB (22657606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746d4353372224213706d143dd92b6b6bb55a75ea19c08d8bf0a1831262fae78`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3131944c8f3aa2bfd1c82fa466a67d152080ddf612067169becafb202be3370`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbcaf71c6e95bc4ab5d255abea93afd44db0486b886ce5701bced2305375566`  
		Last Modified: Thu, 03 Jul 2025 17:23:43 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67da6c0deee4b547055907682ae68fc855d99f2e93d43f6e5b6959c0dd55db5e`  
		Last Modified: Thu, 03 Jul 2025 17:23:45 GMT  
		Size: 22.2 MB (22218098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:47e4025f5f5eb4bb57f9bc7b3c77d306050988fe620d7ee3e7af4720382fe323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28.3.1-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:6fd3a0953d971332397c8e5f14fa538fc9feb8ee0df0761ef69cc664d2c15d5a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542412535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7fb045a7559131f0319249930363ace2c34f3549f5254f962c31ec2b021974`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 03 Jul 2025 17:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:28:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:28:01 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:28:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:28:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:28:17 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:28:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:28:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:28:30 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:28:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8360bc4e45fd1207fbb8507f009f2fafe0c692dda8013b87da385b1687fdb93`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee70f98e67bab9d88bef6785da7dcb0243c6678f90f98f1819bb1d6f15bc400`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 401.7 KB (401674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79844d9fe7e509cc013db5713ac75c91fdef2469815feec90b5b5ccad0760d`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6417f363ada4659759175f87056dac7cb772357f80f942c6f12d9c3a511ae2`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754e9768d552528080346d5f1236df2b7fec0cc26703a72181ab5c56597d3874`  
		Last Modified: Thu, 03 Jul 2025 17:32:16 GMT  
		Size: 20.9 MB (20869952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773798f77aa5f53805ec80969f800c997234c80e3eeaeb70915df160d58698d7`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08de61fa1493600c5c1abb22fb424babbd40f76e25bc0cb27af06a1e6826699`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9638f01c3683753b6296eba7747c7453af7e93065c1727c6b1c271fe3a9ad03`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2aa5bce1514c94a539188e90cbf3433418f9aee7b02aa6196d1b252701f4a6`  
		Last Modified: Thu, 03 Jul 2025 17:32:17 GMT  
		Size: 22.7 MB (22693614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b469a4641279b25c6f4c69230acb7f20cf78488659ef25e4b936f65ad62f7f`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94637a4a498775806b5d83e9b9a5dc8b4630e91f61f2560420791e57745cf4ff`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b5885e19d477e90daf5b71748592e75e7b6b7ff7acedc236c6872db6a7e27`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c38a51f4f1af8ed66ca040eb007a92422ee88d91d4dd660bd0f0f5214c46e7c`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 22.3 MB (22261431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:d623d8d72aa526abcdc996ac8963062a715235ffda58556d864112b8b3fab21b
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
$ docker pull docker@sha256:85b2b37853090b68f2bec9b58a28c514aa4a92821231590662d961ec69ca3bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75408319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0884f72ce3334bfac5c84db32abe1dbd7d6d3b0eaeda1735e8e1c5017582741b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6e8ad138fd78450c30c813f8090cdde12769d5d73beb9c3074783e319a24839d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bceb0017eb30fe94b56cfaebf3348fa544b1440eda09cd6afd8a01f4111633`

```dockerfile
```

-	Layers:
	-	`sha256:665d67252df18d6a5da27a11150b2176a16e3ccfa6892683968a9bd2c30e670c`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a3adc3151b74ccad480eee90a0785c6bbf00ae197b29da17912540a9c6307df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70375532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17419babf75f830d0703a82c44c1ea73abe9ad55bc6ecf940e7b6094ace9dff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:26df6789e84e297b20d944fb722165f5a370ea64e3feab5f200814bcebda2025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0fbbe78fe8f5212ac315d751f274fb1730455ffc3833b07d1aeddd8de82656`

```dockerfile
```

-	Layers:
	-	`sha256:1ffa78e1803982dfe37ed32d4c1bd928dfb46888778cd8bf093da83cd5b55b46`  
		Last Modified: Thu, 03 Jul 2025 20:07:47 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c6088237d22ce9f1c74b09f299ffc9f660ae3d9b0b05cf68e70974559ef0b72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69376189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10eeb922114f57e5118d438eef0c96af65407b628eafbe137c8fdb51fcad1d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4620cfbab6b718b6d7608e646d78fee8bd24e4a9e3998c00d2cdb9fc500a4d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0119c9efe61eb4c2a2315fc24b97f0186bdecc9db92ff39c084e27c154054af`

```dockerfile
```

-	Layers:
	-	`sha256:5ab8fb7ac3eb539be8a1207dcaf14c686d92029c58cf5144592f402daaafb75b`  
		Last Modified: Thu, 03 Jul 2025 20:07:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:345329b66e3b117cfabf618ee56c67a4ce9ee4226ed3bf4b2b62d98e8d15e90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7302f18f8f6a2df7421bf64634eb1a82bab0d8397a5cfeed34f49ad79288594d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6972a69e584db7ee5fb8279874ef80ea710672907c48d4e75432ecec12a692bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36eae856160dae536d39b9a3894bcdd53e6a8515faedf00b3ed1d0b03dff1a6`

```dockerfile
```

-	Layers:
	-	`sha256:1202a1d5f73476f0c58ffdbc17ef1175dc800026e4e305fffb0e8a8f847c4234`  
		Last Modified: Thu, 03 Jul 2025 20:07:57 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:0a2ee60851e1b61a54707476526c4ed48cc55641a17a5cba8a77fb78e7a4742c
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
$ docker pull docker@sha256:af6f4a6f99d3b928aaf2a4c89c92362b61fe5714ce4b359357a7034d72addbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147530306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56629b96a64d6e6a67bb353c4659a5b6bcbe3d1b5d839623c78e3fbfb5d5d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:f284b77d89a52d6e50f665a70dc9cba7676d350135900856dffad8fa83381129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a60b03d224867bf21b8fcdbedf71f4b988ef38df593113cf167071ae0db1ba`

```dockerfile
```

-	Layers:
	-	`sha256:de6313881469a25f3e98fd3e7a03e6f441046c278766a4991497c229caa95ca8`  
		Last Modified: Thu, 03 Jul 2025 20:07:32 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1a2b90b79d231f6d79b223f7f6148732566e4f6c8051b02ed9dbb8442cfcd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138128973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7996c20d4b7e0501900c77f11b3517bdde8df963fd95bca52f74102cbee16037`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c35411abd7ff8741d102086e57d13dcf53a36b38d0f83d70dfc564451c476f`  
		Last Modified: Thu, 03 Jul 2025 18:07:38 GMT  
		Size: 9.5 MB (9461151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4334023f752ea84943589c958d76280ad68320a22b65a8b28032bfef145a87`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 90.1 KB (90064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6838b2f15e318a3756e830fe9328c98594e76f559f183a6a2a82f247414e7`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af830fec2f9b00ff6031aa3b5abf77926f1f8ec61c43c2fd933a53aeec3b9716`  
		Last Modified: Thu, 03 Jul 2025 18:07:40 GMT  
		Size: 58.2 MB (58196228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caaa15e0a3e27f74ea0cdc96286507cdae37c6b9da9f6dd58b75262174e04c`  
		Last Modified: Thu, 03 Jul 2025 18:07:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5519b7b6fb48cbf0f06bcb48d96dac6ae50d2f29df217e3ed905c33cfab0f0ff`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:9fbda7207e684fc22b48dcb3d1cb9b90be4e59a79e8f051557e013f5098a80e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f6cfed87f8a2540111bff41a1e80f225970a9299f983f4513c8cb7bc11b3d3`

```dockerfile
```

-	Layers:
	-	`sha256:cefef8bf5e16c3e687c0fa2dec76440f45a5dfecfd26a50caecaeff9ca6c7528`  
		Last Modified: Thu, 03 Jul 2025 20:07:36 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:73e517576082f7d56a5d5d498e3213393339b90ec3f7b5716b77e74da9a7dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136275323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e52499045af79026f3a96eb634a83bcbfcc05f78d5156c2a02d7d17434ed51`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8283e24f943182f28dc30d039850e13d96eafad82bb6c22a140c3efe652058c1`  
		Last Modified: Thu, 03 Jul 2025 18:08:05 GMT  
		Size: 8.6 MB (8610439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450a67de7fa2fbc5711e2fdfa60c7a2945e5a35ffe63f7bc37853d0460923`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 86.5 KB (86500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9b557ed7aa7cbe6b15891cd15a970a5153869d665c096b93ce12aba19709c`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5256c88f5ca619407e171fec8e2327d32bdbb28ff0039389c324c0957d51e2a7`  
		Last Modified: Thu, 03 Jul 2025 18:08:13 GMT  
		Size: 58.2 MB (58196195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5ad95ba8e852e939d06670a567addbe1f7545dfcf9cc2f0bc72df2a549f192`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9ec3f7bf60f8287e8fb6b564e36112f40c678b0a2419e630d97e2eee47d12`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:676399e8815c91e2f684422dcc72561d36f8b71d0a31afa4f8167e54862d165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47da4f2e8332513e7f2fd9f4207d0b2046cb012304e8af3010c40bc64f11e5e8`

```dockerfile
```

-	Layers:
	-	`sha256:e377a69875e60adb621efef5a8aca158b3dafb7230b4f16619be0970236a7d43`  
		Last Modified: Thu, 03 Jul 2025 20:07:39 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9091b93a0497a742433859af71e9d2cbf91a04b4f8b463b2a3ac7bccf626b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138567854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7777fe83512e386382fb92ecdee5fab02657d37d0e4f5c421aa77b3a7e64c3b6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:0a04bc025db0198b912fa1aaba813b1f2e18956dd246940e2a1e7fc2edc56a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b366a219a7150c173e76372f82ae9e34c8c02de7aa62cb30dd1b0d33c196573c`

```dockerfile
```

-	Layers:
	-	`sha256:3650e92878e003d91cb996c90670a5c4fc7f62157f8338da233bf84fee665245`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:b44749d9b6aba4f5f80bb759bb6ea83e62a1f2c8c0897ad059c5eeafb8d43c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:db4c04bc4465b0434d622bf882950ce45685a378b0ee811e9e1b1219ba6e9436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168515988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21511f843dd54e89f5b101840d8b53c72e1c5ddcd62a5f854485baaa6600fa9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b828347c2a041335957c90cb55b04a323af16f817d2ea2aaa04c38fd9e0a915b`  
		Last Modified: Thu, 03 Jul 2025 18:11:38 GMT  
		Size: 3.4 MB (3398182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9015f88f20407c97d95eec2557adffa39da70fe898e9ef54cc056e91f839250`  
		Last Modified: Thu, 03 Jul 2025 18:11:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fe64c2be9d18d459bedfb0eaae711ac691aae9da049d2259fa61694eebd252`  
		Last Modified: Thu, 03 Jul 2025 18:11:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6974db92eb03859ebac691c35b3b8e4bda756d27667351ec08ad27e3cebb426`  
		Last Modified: Thu, 03 Jul 2025 18:11:40 GMT  
		Size: 17.6 MB (17586158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69244f3e5323c1ad99d83700a10a30cbf3c9b59bd1d6deeb518016c91586411e`  
		Last Modified: Thu, 03 Jul 2025 18:11:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a0cc335b94ca365a19094d5303c10b30b5b1662788b30690d3a98d802427f0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d20f1d9888c19a6d1afdef8729e43aec20f90f322855e9b5c650247836ff0c`

```dockerfile
```

-	Layers:
	-	`sha256:e2532b0be60f5ccad634be0410f2b01c3922c3e42bfc227d2e206c65d2636109`  
		Last Modified: Thu, 03 Jul 2025 20:07:54 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5cedcdbd876edad79f8f62fec3ae650536577aa61a559acaa654dc6f6af631b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159976175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c81ca73fc3e1d219a425a73736a34d915776a8259e79eedd00597f482971cc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055439fa6d8fcc51af0c10bf7bc294b0e1f51845f1fdf975c6f2ed005a72dd7`  
		Last Modified: Thu, 03 Jul 2025 18:22:09 GMT  
		Size: 3.4 MB (3389671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5a4b35eded985f79fbbe8910bab2457acf21a3a5174dc98c50b5a52d6ae94c`  
		Last Modified: Thu, 03 Jul 2025 18:22:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a53aeca772b1453a3107bc47c8fa4c0a699b795f5bb46ce8147903629091105`  
		Last Modified: Thu, 03 Jul 2025 18:22:08 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae30160e013cd77a67fb1c70bca1161363b6d03b329bdbacdb070411f5fab194`  
		Last Modified: Thu, 03 Jul 2025 18:22:10 GMT  
		Size: 18.0 MB (18017309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156b018b4075be77289b3748988b7f34a0e22844508c688dcb3d3fbf47cba9c5`  
		Last Modified: Thu, 03 Jul 2025 18:22:08 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f92dbdaa152a7b0b5985bc9fb607ae59b1f53293d7e03ed0a763bfdb11d65c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e0049363c6bc42c7778de09c867a855ecc9d304eed6f5197c9c0be01a92207`

```dockerfile
```

-	Layers:
	-	`sha256:ddb6058b675b6f844f3eeb5728ee724318dd9b2b36a6a2ac8c90f51f2a3f80a3`  
		Last Modified: Thu, 03 Jul 2025 20:07:57 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:0a2ee60851e1b61a54707476526c4ed48cc55641a17a5cba8a77fb78e7a4742c
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
$ docker pull docker@sha256:af6f4a6f99d3b928aaf2a4c89c92362b61fe5714ce4b359357a7034d72addbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147530306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56629b96a64d6e6a67bb353c4659a5b6bcbe3d1b5d839623c78e3fbfb5d5d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:f284b77d89a52d6e50f665a70dc9cba7676d350135900856dffad8fa83381129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a60b03d224867bf21b8fcdbedf71f4b988ef38df593113cf167071ae0db1ba`

```dockerfile
```

-	Layers:
	-	`sha256:de6313881469a25f3e98fd3e7a03e6f441046c278766a4991497c229caa95ca8`  
		Last Modified: Thu, 03 Jul 2025 20:07:32 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:1a2b90b79d231f6d79b223f7f6148732566e4f6c8051b02ed9dbb8442cfcd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138128973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7996c20d4b7e0501900c77f11b3517bdde8df963fd95bca52f74102cbee16037`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b98221bb2ef819f65acc6ec772fd69aa796ab0ca333abb04450d868f73f4f89`  
		Last Modified: Thu, 03 Jul 2025 17:29:11 GMT  
		Size: 20.0 MB (20011489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca59b0a48d478a976ac3c39843ba5ea7dbacb990e24e9f866955ecda8e81d0c`  
		Last Modified: Thu, 03 Jul 2025 17:29:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b8fc64173234d850fc230135e03328d1b0271419d17a7c231bcd5963fda99`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bbc48ed5a489a5c55075e8989fb5e90bd8f1cc1a720b9c9fa7af58387c595`  
		Last Modified: Thu, 03 Jul 2025 17:29:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c35411abd7ff8741d102086e57d13dcf53a36b38d0f83d70dfc564451c476f`  
		Last Modified: Thu, 03 Jul 2025 18:07:38 GMT  
		Size: 9.5 MB (9461151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4334023f752ea84943589c958d76280ad68320a22b65a8b28032bfef145a87`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 90.1 KB (90064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6838b2f15e318a3756e830fe9328c98594e76f559f183a6a2a82f247414e7`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af830fec2f9b00ff6031aa3b5abf77926f1f8ec61c43c2fd933a53aeec3b9716`  
		Last Modified: Thu, 03 Jul 2025 18:07:40 GMT  
		Size: 58.2 MB (58196228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caaa15e0a3e27f74ea0cdc96286507cdae37c6b9da9f6dd58b75262174e04c`  
		Last Modified: Thu, 03 Jul 2025 18:07:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5519b7b6fb48cbf0f06bcb48d96dac6ae50d2f29df217e3ed905c33cfab0f0ff`  
		Last Modified: Thu, 03 Jul 2025 18:07:37 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:9fbda7207e684fc22b48dcb3d1cb9b90be4e59a79e8f051557e013f5098a80e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f6cfed87f8a2540111bff41a1e80f225970a9299f983f4513c8cb7bc11b3d3`

```dockerfile
```

-	Layers:
	-	`sha256:cefef8bf5e16c3e687c0fa2dec76440f45a5dfecfd26a50caecaeff9ca6c7528`  
		Last Modified: Thu, 03 Jul 2025 20:07:36 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:73e517576082f7d56a5d5d498e3213393339b90ec3f7b5716b77e74da9a7dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136275323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e52499045af79026f3a96eb634a83bcbfcc05f78d5156c2a02d7d17434ed51`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8283e24f943182f28dc30d039850e13d96eafad82bb6c22a140c3efe652058c1`  
		Last Modified: Thu, 03 Jul 2025 18:08:05 GMT  
		Size: 8.6 MB (8610439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450a67de7fa2fbc5711e2fdfa60c7a2945e5a35ffe63f7bc37853d0460923`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 86.5 KB (86500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9b557ed7aa7cbe6b15891cd15a970a5153869d665c096b93ce12aba19709c`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5256c88f5ca619407e171fec8e2327d32bdbb28ff0039389c324c0957d51e2a7`  
		Last Modified: Thu, 03 Jul 2025 18:08:13 GMT  
		Size: 58.2 MB (58196195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5ad95ba8e852e939d06670a567addbe1f7545dfcf9cc2f0bc72df2a549f192`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9ec3f7bf60f8287e8fb6b564e36112f40c678b0a2419e630d97e2eee47d12`  
		Last Modified: Thu, 03 Jul 2025 18:08:03 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:676399e8815c91e2f684422dcc72561d36f8b71d0a31afa4f8167e54862d165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47da4f2e8332513e7f2fd9f4207d0b2046cb012304e8af3010c40bc64f11e5e8`

```dockerfile
```

-	Layers:
	-	`sha256:e377a69875e60adb621efef5a8aca158b3dafb7230b4f16619be0970236a7d43`  
		Last Modified: Thu, 03 Jul 2025 20:07:39 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9091b93a0497a742433859af71e9d2cbf91a04b4f8b463b2a3ac7bccf626b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138567854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7777fe83512e386382fb92ecdee5fab02657d37d0e4f5c421aa77b3a7e64c3b6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:0a04bc025db0198b912fa1aaba813b1f2e18956dd246940e2a1e7fc2edc56a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b366a219a7150c173e76372f82ae9e34c8c02de7aa62cb30dd1b0d33c196573c`

```dockerfile
```

-	Layers:
	-	`sha256:3650e92878e003d91cb996c90670a5c4fc7f62157f8338da233bf84fee665245`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:7bc3cbaeffb673a3857fad815ce1bc01a5ffe74778eeb337ad55c118c72f836a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:6fd3a0953d971332397c8e5f14fa538fc9feb8ee0df0761ef69cc664d2c15d5a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542412535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7fb045a7559131f0319249930363ace2c34f3549f5254f962c31ec2b021974`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 03 Jul 2025 17:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:28:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:28:01 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:28:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:28:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:28:17 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:28:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:28:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:28:30 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:28:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8360bc4e45fd1207fbb8507f009f2fafe0c692dda8013b87da385b1687fdb93`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee70f98e67bab9d88bef6785da7dcb0243c6678f90f98f1819bb1d6f15bc400`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 401.7 KB (401674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79844d9fe7e509cc013db5713ac75c91fdef2469815feec90b5b5ccad0760d`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6417f363ada4659759175f87056dac7cb772357f80f942c6f12d9c3a511ae2`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754e9768d552528080346d5f1236df2b7fec0cc26703a72181ab5c56597d3874`  
		Last Modified: Thu, 03 Jul 2025 17:32:16 GMT  
		Size: 20.9 MB (20869952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773798f77aa5f53805ec80969f800c997234c80e3eeaeb70915df160d58698d7`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08de61fa1493600c5c1abb22fb424babbd40f76e25bc0cb27af06a1e6826699`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9638f01c3683753b6296eba7747c7453af7e93065c1727c6b1c271fe3a9ad03`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2aa5bce1514c94a539188e90cbf3433418f9aee7b02aa6196d1b252701f4a6`  
		Last Modified: Thu, 03 Jul 2025 17:32:17 GMT  
		Size: 22.7 MB (22693614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b469a4641279b25c6f4c69230acb7f20cf78488659ef25e4b936f65ad62f7f`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94637a4a498775806b5d83e9b9a5dc8b4630e91f61f2560420791e57745cf4ff`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b5885e19d477e90daf5b71748592e75e7b6b7ff7acedc236c6872db6a7e27`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c38a51f4f1af8ed66ca040eb007a92422ee88d91d4dd660bd0f0f5214c46e7c`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 22.3 MB (22261431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:0dfbb2cb73e0f119f7827c4294818bae9e2b593f4f499366be7ab74496416a06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346334126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2405e622d57138fe3077ec39b9f3f42ebcd0cfdf09f47419ba243ae7fdd5b79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 03 Jul 2025 17:22:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:22:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:22:33 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:22:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:22:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:22:51 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:22:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:22:53 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:23:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:23:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:23:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:23:11 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:23:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b61b501a45983587b82cbf3ec9a02d5dc816be481f91442c358c854092ae35f`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f44a2afa65d60b4bf8e64db5fe87206c5d6caea4df5f91ab8520f7775c6108`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 361.4 KB (361411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a33626ee108dfe569f1ac806973edaad156af082da5adb5cdc619d671c92af`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415464cc927cf6550b8b02ab9a1c7d7076b523ce7f3eb3d6cb06af3cb0717cd`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece6c486f7a91317125ee5a8a9703bd97ad6fe62ffa3eed7300b64d6dae5658c`  
		Last Modified: Thu, 03 Jul 2025 17:23:46 GMT  
		Size: 20.8 MB (20833794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cca4e9c6c6042835085a7bec40bfedfff801d6a5bb1c55fd0d69f3cb4224c5`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e45039c40258e0ad1ddc66ea6789239b16daa6e4b25ad6133a2a0f9155e84e`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d056b131a087efcd1c66a659d7faab0e72b58a72df8d673e794b12df4133e2`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec084cd1ecfecc49f2aee4ece051aaf3b0e26d486dc4f206b8cdca3c459bbba3`  
		Last Modified: Thu, 03 Jul 2025 17:23:44 GMT  
		Size: 22.7 MB (22657606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746d4353372224213706d143dd92b6b6bb55a75ea19c08d8bf0a1831262fae78`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3131944c8f3aa2bfd1c82fa466a67d152080ddf612067169becafb202be3370`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbcaf71c6e95bc4ab5d255abea93afd44db0486b886ce5701bced2305375566`  
		Last Modified: Thu, 03 Jul 2025 17:23:43 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67da6c0deee4b547055907682ae68fc855d99f2e93d43f6e5b6959c0dd55db5e`  
		Last Modified: Thu, 03 Jul 2025 17:23:45 GMT  
		Size: 22.2 MB (22218098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3b16a51f7b350f70417bf9bd061388412d4fe13605c264cd3965ad44c040b98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:0dfbb2cb73e0f119f7827c4294818bae9e2b593f4f499366be7ab74496416a06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346334126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2405e622d57138fe3077ec39b9f3f42ebcd0cfdf09f47419ba243ae7fdd5b79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 03 Jul 2025 17:22:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:22:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:22:33 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:22:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:22:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:22:51 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:22:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:22:53 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:23:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:23:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:23:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:23:11 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:23:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b61b501a45983587b82cbf3ec9a02d5dc816be481f91442c358c854092ae35f`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f44a2afa65d60b4bf8e64db5fe87206c5d6caea4df5f91ab8520f7775c6108`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 361.4 KB (361411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a33626ee108dfe569f1ac806973edaad156af082da5adb5cdc619d671c92af`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415464cc927cf6550b8b02ab9a1c7d7076b523ce7f3eb3d6cb06af3cb0717cd`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece6c486f7a91317125ee5a8a9703bd97ad6fe62ffa3eed7300b64d6dae5658c`  
		Last Modified: Thu, 03 Jul 2025 17:23:46 GMT  
		Size: 20.8 MB (20833794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cca4e9c6c6042835085a7bec40bfedfff801d6a5bb1c55fd0d69f3cb4224c5`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e45039c40258e0ad1ddc66ea6789239b16daa6e4b25ad6133a2a0f9155e84e`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d056b131a087efcd1c66a659d7faab0e72b58a72df8d673e794b12df4133e2`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec084cd1ecfecc49f2aee4ece051aaf3b0e26d486dc4f206b8cdca3c459bbba3`  
		Last Modified: Thu, 03 Jul 2025 17:23:44 GMT  
		Size: 22.7 MB (22657606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746d4353372224213706d143dd92b6b6bb55a75ea19c08d8bf0a1831262fae78`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3131944c8f3aa2bfd1c82fa466a67d152080ddf612067169becafb202be3370`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbcaf71c6e95bc4ab5d255abea93afd44db0486b886ce5701bced2305375566`  
		Last Modified: Thu, 03 Jul 2025 17:23:43 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67da6c0deee4b547055907682ae68fc855d99f2e93d43f6e5b6959c0dd55db5e`  
		Last Modified: Thu, 03 Jul 2025 17:23:45 GMT  
		Size: 22.2 MB (22218098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:47e4025f5f5eb4bb57f9bc7b3c77d306050988fe620d7ee3e7af4720382fe323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:6fd3a0953d971332397c8e5f14fa538fc9feb8ee0df0761ef69cc664d2c15d5a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542412535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7fb045a7559131f0319249930363ace2c34f3549f5254f962c31ec2b021974`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 03 Jul 2025 17:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:28:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:28:01 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:28:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:28:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:28:17 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:28:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:28:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:28:30 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:28:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8360bc4e45fd1207fbb8507f009f2fafe0c692dda8013b87da385b1687fdb93`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee70f98e67bab9d88bef6785da7dcb0243c6678f90f98f1819bb1d6f15bc400`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 401.7 KB (401674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79844d9fe7e509cc013db5713ac75c91fdef2469815feec90b5b5ccad0760d`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6417f363ada4659759175f87056dac7cb772357f80f942c6f12d9c3a511ae2`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754e9768d552528080346d5f1236df2b7fec0cc26703a72181ab5c56597d3874`  
		Last Modified: Thu, 03 Jul 2025 17:32:16 GMT  
		Size: 20.9 MB (20869952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773798f77aa5f53805ec80969f800c997234c80e3eeaeb70915df160d58698d7`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08de61fa1493600c5c1abb22fb424babbd40f76e25bc0cb27af06a1e6826699`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9638f01c3683753b6296eba7747c7453af7e93065c1727c6b1c271fe3a9ad03`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2aa5bce1514c94a539188e90cbf3433418f9aee7b02aa6196d1b252701f4a6`  
		Last Modified: Thu, 03 Jul 2025 17:32:17 GMT  
		Size: 22.7 MB (22693614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b469a4641279b25c6f4c69230acb7f20cf78488659ef25e4b936f65ad62f7f`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94637a4a498775806b5d83e9b9a5dc8b4630e91f61f2560420791e57745cf4ff`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b5885e19d477e90daf5b71748592e75e7b6b7ff7acedc236c6872db6a7e27`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c38a51f4f1af8ed66ca040eb007a92422ee88d91d4dd660bd0f0f5214c46e7c`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 22.3 MB (22261431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
