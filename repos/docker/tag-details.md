<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:27`](#docker27)
-	[`docker:27-cli`](#docker27-cli)
-	[`docker:27-dind`](#docker27-dind)
-	[`docker:27-dind-rootless`](#docker27-dind-rootless)
-	[`docker:27-windowsservercore`](#docker27-windowsservercore)
-	[`docker:27-windowsservercore-1809`](#docker27-windowsservercore-1809)
-	[`docker:27-windowsservercore-ltsc2022`](#docker27-windowsservercore-ltsc2022)
-	[`docker:27.4`](#docker274)
-	[`docker:27.4-cli`](#docker274-cli)
-	[`docker:27.4-dind`](#docker274-dind)
-	[`docker:27.4-dind-rootless`](#docker274-dind-rootless)
-	[`docker:27.4-windowsservercore`](#docker274-windowsservercore)
-	[`docker:27.4-windowsservercore-1809`](#docker274-windowsservercore-1809)
-	[`docker:27.4-windowsservercore-ltsc2022`](#docker274-windowsservercore-ltsc2022)
-	[`docker:27.4.0`](#docker2740)
-	[`docker:27.4.0-alpine3.21`](#docker2740-alpine321)
-	[`docker:27.4.0-cli`](#docker2740-cli)
-	[`docker:27.4.0-cli-alpine3.21`](#docker2740-cli-alpine321)
-	[`docker:27.4.0-dind`](#docker2740-dind)
-	[`docker:27.4.0-dind-alpine3.21`](#docker2740-dind-alpine321)
-	[`docker:27.4.0-dind-rootless`](#docker2740-dind-rootless)
-	[`docker:27.4.0-windowsservercore`](#docker2740-windowsservercore)
-	[`docker:27.4.0-windowsservercore-1809`](#docker2740-windowsservercore-1809)
-	[`docker:27.4.0-windowsservercore-ltsc2022`](#docker2740-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:27`

```console
$ docker pull docker@sha256:6ca9a6811085e2cf769cbac04bc47daf66629102990391caab7cf37426e939da
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
$ docker pull docker@sha256:36f7e13d969ec9bffe8d2700da5168c1e1bc69cb1e25dca50bfe9591db4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (135026509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37123e40ec5295ac68158ace2d5c302a8a5d33f6e40b9a3397be063f941d3705`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99c836815720eb35e0ac10baba1a625902fa8619ab24dbacb464e77b5621e4`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 7.9 MB (7889946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441473b54564f25321bb746ad1ece9e72511542e0e2cf2d6c4a685d55642042f`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b67a33361a7355f408f37f39fba74992e5a77bad7adfbfeb50867380ee2058`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db7f9329b5aa8a8e730800809a97cdbd9afc59ceb4e4ecdaf48b1292ef8247e`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.8 MB (18797158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d946c4c96d3bb716e1307d14a988d350554bf9683300d19cb603834ba7f70b43`  
		Last Modified: Wed, 04 Dec 2024 00:29:14 GMT  
		Size: 19.2 MB (19188666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91324bcb958d9893a36d0a635b1b119c08ecf5aeea0c33a8933695c558b1f15`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa70352df20029e281f85627f717681287f1c2ad199e13366e98afddf22ba20`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dc30100905c3dd4f8be02226d67905079d48b660f5131a0bdb9ac5b53ec318`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b7affd2cbd2d63776ef3a56b1e8e87bbe6c4ff45926945f9d0bd59a70fbc8a`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 9.1 MB (9067299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b563b244ec69075f74c96a055589724459ad7cf3e1dd2fe88db465ecf4d906ff`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 89.2 KB (89239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0d3672080b087610cc6e91768c0cf10636fa7f019a0df3ac2a20b3a93344b`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9a91997e3508e37720f5db1be866b04d023f042b900dd7ceac9d60489a8af3`  
		Last Modified: Wed, 04 Dec 2024 01:28:36 GMT  
		Size: 57.8 MB (57798931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efa22532f8b3bec3ec076779c6ad758bc7e8068de8736d2eb0eeb51c20c763d`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78f3fd7b6197e4187d96cdb25a2436872c022b3c665cbad20d48b3abfb9853`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:3b16f4d38590b89620d50f77fea6ac71e3e62f7009693ebc9a309dfb104b3942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b187b4999b26b9e4634e31634862a675a485c82687b846ad67d258920d1e5865`

```dockerfile
```

-	Layers:
	-	`sha256:e1fe188fc168b4b977096e6aa2b3e2c91716308c54bcffe967c4e398f8058419`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:bc484346674dbccdad51e302aeba0ac06e9d3650dfaf52a4961515c80f79c5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125903353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe332abc325288026bb27880b82475f8a713e552c7fa06958233fbc392385be`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dec1f3e06da3f8757b7ab0c912b2790b19463c9e38b2e62db7016713ec835a`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 7.8 MB (7820557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42de83cdff8ecb35d376bef426a487ec59cb3c6e47646a152914957e84298f0d`  
		Last Modified: Tue, 12 Nov 2024 02:19:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7e03894c45574eb692f15e4d6931a5483f1332581f7edad8bd3d3aa28078a4`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 16.6 MB (16601553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416b9ce4eadc755f144844cbf118e90f4562ea751a4b3a7d5cbdf3ef493d2a6a`  
		Last Modified: Wed, 04 Dec 2024 00:29:28 GMT  
		Size: 17.4 MB (17446678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f851db5c0708c729bed8901e10a62c5b08c100e328b7e0c98a25452f22134533`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 18.0 MB (18000429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6022bb89098191f5e257aa4e32bcfa33c5ad77af1820164d53a2d23a155c1efb`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e5a5238bf0b1dc3a4eee05c5847d1c25e2d05a3872672ff9030a6e39564f2`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e341b6cbf0b1d0892b191cafb94e2bb674ea7086b15fb46fddcfc0a87a0950`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37118131d8c6abc8a1d2bc3d06b19e716aba85bd70ef596e731912b3263caf68`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 9.1 MB (9060142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808ad8667e97e661f5dbf6ef2725dc1e89602f0c51f25e110c1d5d182a490c6`  
		Last Modified: Wed, 04 Dec 2024 01:28:49 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11440987ff8e3e813048fee3b7b704ec574022260dbe66591f9cd4b8c43dcd9c`  
		Last Modified: Wed, 04 Dec 2024 01:28:49 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c7b913e1f09d88e471b3909933b4992191770bb8f0d7987e9407b55d8f4b29`  
		Last Modified: Wed, 04 Dec 2024 01:28:52 GMT  
		Size: 53.5 MB (53511021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad8d0c2d6a8178e298e85ba96d6d2718f7046df88dfd0f2acf48946a20f6f1`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b4367498a260de054f3ab7caa2301f404535c5be8ceb9af00fc820a6d010a8`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:0528ca2fa8acf242eac680e7dc3b059e769d47969412203ef9b30b692461f64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2eada113d5f4c8076d65858800c094e7761c0da275e0aeecccb35c15a583d83`

```dockerfile
```

-	Layers:
	-	`sha256:748bd2a8690fba2669cd29c9ba34cb8e69cbb5c5ca2a9e7b12ff0f0209d19674`  
		Last Modified: Wed, 04 Dec 2024 01:28:48 GMT  
		Size: 34.7 KB (34730 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:4282a706d0de62d1870d0748595012675b214e349123d04f8b28047f95fe7bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124083382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cd6b3959c6bdcfe0c15f185deaad456030912d24466023e92da5839f19c077`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a8d373266083cffcbf2a6623223d8b2c780180ffc25c641834fa0f399b861c`  
		Last Modified: Wed, 04 Dec 2024 07:15:41 GMT  
		Size: 7.2 MB (7153539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ecea7f1649dbef369192500f3eda21b1f30ba448ca4b382f6dc90ba4b77ed6`  
		Last Modified: Wed, 04 Dec 2024 07:15:40 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8345cbaadf649b7179d374408307a49de91dcad20d33264ff67e18f1df31ad`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 16.6 MB (16591541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0a479bcd6279df331f32a4aab4c0c1f2140ff8ad6863ac2e92df68745f4212`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 17.4 MB (17426318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bda8e0c337df3901bcac5c617da87c4374d34e45d2442c84e52a57079226`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 18.0 MB (17984726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922d604be17f4bbd00d6ed640b5b13212bb106fd9e1de0c22b96b23de6b53f8f`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f87b589e7a688691cd8e51d42d71f370527d4b4710084733eb6d3a885f95c8`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dbeec76024b177d0212c7c8e652f88917461283d8538caf5e1b7120885f229`  
		Last Modified: Wed, 04 Dec 2024 07:16:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87469764160593846c30c8e28dac1080459b4051932d74fd34db73c0027d0565`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 8.2 MB (8228295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba34f50361e4b02b179eb03250dade6609581cc47552001b3b992c82798031d`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 84.5 KB (84498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a38bc738f51a41a50f63665a4183c459cf953d52052327d82e14c4fc2d069a`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38510939bc5659853d67592adbfba6d41d4f83a34c086b45ca197351df04db42`  
		Last Modified: Wed, 04 Dec 2024 09:58:59 GMT  
		Size: 53.5 MB (53511037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca93ad33ff91f6aaf58315b3c74581ce07d1f79488e6b309946a372f1928266`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cf7c178aa1938ea5f4c2b273d58b83721fe1c7133e13e05e37da3dd1b36839`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:5060a914795d4ad7da1ec0b4baaa83c418aed4aa32a77f3269faa0676cf4ef54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56e35531d708cdb1857fb999b927304860627396f593f2f6bc9a5f8d9940760`

```dockerfile
```

-	Layers:
	-	`sha256:dda6401da3e01b40934462451eae7cf3f9e919ee3b1f51514bdb8af45a26d9dc`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 34.7 KB (34730 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4d045d01ee7e2c931e74d17300e3e1994aa561841fc20f2323c64f36dcb6b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127617087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa4bd8f7eb76767555fa9b4fcfad991cb6ce4d97f38b7f5d83778b35ca10143`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4036cbb7a2e5b8a0ce714e4d08fbb64576b80cdd256ff9f0cba6473d73c3d`  
		Last Modified: Wed, 04 Dec 2024 01:35:25 GMT  
		Size: 8.0 MB (7998285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60d77d28745a9052470e2cbb96a13d33e0a0e02f2499098e3d150ae69df6ec1`  
		Last Modified: Wed, 04 Dec 2024 01:35:24 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91ef372941d329672b67f1838f7226808a97f8e58397715e78cd330e0868a9`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd17f2da053085769cb4bd5050acf30ee866b24423db4f6a4501542ff3c577e`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.1 MB (17094301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bf40ee41c170bda856abc36f41024d06b357a9952ada38b13eaa38f5e4fb42`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17533136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28d3c43303886712330874ba9a1a16c23148a9c3d9473bf8a713a8daaa7fab`  
		Last Modified: Wed, 04 Dec 2024 01:35:43 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37013ffc205c5864e92c2dcb7e0f270522f1567a8aa872a4387741223a709686`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ffff7c773efbee73c878f22b1180466f0913d6bf9c789fc84e7327463c4b72`  
		Last Modified: Wed, 04 Dec 2024 01:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91e6f6ccb3fb7cbb88f239f42c64aada23404c0c4dce018a70293397b6a7bb2`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 9.9 MB (9854884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b149a083ef4ec99e387305c4f67b50322dca8423ae3768a35f45a2fd271e4f`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 98.7 KB (98661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ba97446cb2349c7c7ede5bac8c57eb62af7c4ed374b72d5c63231122fd3f3e`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c66d82acbf0c58afe05ed4bd7a0e5537ad2a7247cc27a922ca66d5aa62748`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487d2d57a72d0f05061f16b8670991e34849ece621911b2e3501cab1ed7f5ea9`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86120177f87d9b796dce95a7af9473e7763db7ce5380f3ef778d258d244a6c3d`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:53bbd101f17d09cd1cfbce5f9d4ae4d10faf7dea03558020c7bc7b0841655918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239273cc8f9eddd75eaf9bb9f6385ed96d3efeb918b400d9f49b8566fa417e8d`

```dockerfile
```

-	Layers:
	-	`sha256:e8f2b79a35f2afff1c0161dc8445fc1323b9a1ee36026f95eebda18988ec71dc`  
		Last Modified: Wed, 04 Dec 2024 05:06:38 GMT  
		Size: 34.8 KB (34790 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:328eb399a065780c2cebe9224de003aa14084cf69efae882ac27430f921819b7
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
$ docker pull docker@sha256:f2fb6f02004bd10aaa1b489d19e68f3225aa55c93ad296d322be523911b8664a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68065244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f761a0f3cfe5fb6c1318ed49c84bbb30ba0dd1d7a9c7a619329147cf025b0c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Dec 2024 22:20:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99c836815720eb35e0ac10baba1a625902fa8619ab24dbacb464e77b5621e4`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 7.9 MB (7889946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441473b54564f25321bb746ad1ece9e72511542e0e2cf2d6c4a685d55642042f`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b67a33361a7355f408f37f39fba74992e5a77bad7adfbfeb50867380ee2058`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db7f9329b5aa8a8e730800809a97cdbd9afc59ceb4e4ecdaf48b1292ef8247e`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.8 MB (18797158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d946c4c96d3bb716e1307d14a988d350554bf9683300d19cb603834ba7f70b43`  
		Last Modified: Wed, 04 Dec 2024 00:29:14 GMT  
		Size: 19.2 MB (19188666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91324bcb958d9893a36d0a635b1b119c08ecf5aeea0c33a8933695c558b1f15`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa70352df20029e281f85627f717681287f1c2ad199e13366e98afddf22ba20`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dc30100905c3dd4f8be02226d67905079d48b660f5131a0bdb9ac5b53ec318`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:28b2a9a1c41faefd01e667161876764eb1585c01198ce6a9fadf02876114084e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5fbbd12270145b2fe25952cd19c6f7dadaf0bbb16a703a91da3c67c77f52fe`

```dockerfile
```

-	Layers:
	-	`sha256:0ef8d39d9caf19a29683d5f428c541269a025b580dc6c79972ca68cc0abb9191`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:bd6b01e7e15db48211c58491f5ab02744ee75b8c72a3c9b3f1ae774c2bfe4fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63237978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5417cde1ea6bf81d248fc4a90c9580aee1e0c8c66dc3e0efe2ccb6754745d999`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Dec 2024 22:20:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dec1f3e06da3f8757b7ab0c912b2790b19463c9e38b2e62db7016713ec835a`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 7.8 MB (7820557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42de83cdff8ecb35d376bef426a487ec59cb3c6e47646a152914957e84298f0d`  
		Last Modified: Tue, 12 Nov 2024 02:19:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7e03894c45574eb692f15e4d6931a5483f1332581f7edad8bd3d3aa28078a4`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 16.6 MB (16601553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416b9ce4eadc755f144844cbf118e90f4562ea751a4b3a7d5cbdf3ef493d2a6a`  
		Last Modified: Wed, 04 Dec 2024 00:29:28 GMT  
		Size: 17.4 MB (17446678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f851db5c0708c729bed8901e10a62c5b08c100e328b7e0c98a25452f22134533`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 18.0 MB (18000429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6022bb89098191f5e257aa4e32bcfa33c5ad77af1820164d53a2d23a155c1efb`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e5a5238bf0b1dc3a4eee05c5847d1c25e2d05a3872672ff9030a6e39564f2`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e341b6cbf0b1d0892b191cafb94e2bb674ea7086b15fb46fddcfc0a87a0950`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:40edb31e4f25fd23bb7a242cef0277168fdb7c2928efad81eccf6b64973ffde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d27ae93b0cb111b4172a77c7836f3898a3d6235cbfdf8a277229f783fa5f4f`

```dockerfile
```

-	Layers:
	-	`sha256:dd6ac4f9bb23336484e3057f20ee57df54cbc347925af0095edfb3c06ba0b7f3`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:e87ad798b53baef6d90b5c44af8303ab6cd0ef49e2abab0729d6f151d8071369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62253760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c8f13ab34b5cb8d9487941ad1be49ff1e82f2564a275b559aeac8aabc4d7f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Dec 2024 22:20:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a8d373266083cffcbf2a6623223d8b2c780180ffc25c641834fa0f399b861c`  
		Last Modified: Wed, 04 Dec 2024 07:15:41 GMT  
		Size: 7.2 MB (7153539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ecea7f1649dbef369192500f3eda21b1f30ba448ca4b382f6dc90ba4b77ed6`  
		Last Modified: Wed, 04 Dec 2024 07:15:40 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8345cbaadf649b7179d374408307a49de91dcad20d33264ff67e18f1df31ad`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 16.6 MB (16591541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0a479bcd6279df331f32a4aab4c0c1f2140ff8ad6863ac2e92df68745f4212`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 17.4 MB (17426318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bda8e0c337df3901bcac5c617da87c4374d34e45d2442c84e52a57079226`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 18.0 MB (17984726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922d604be17f4bbd00d6ed640b5b13212bb106fd9e1de0c22b96b23de6b53f8f`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f87b589e7a688691cd8e51d42d71f370527d4b4710084733eb6d3a885f95c8`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dbeec76024b177d0212c7c8e652f88917461283d8538caf5e1b7120885f229`  
		Last Modified: Wed, 04 Dec 2024 07:16:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a2e1f67dc70fae764b891ca53c791a1e606c473bf557dc90c21957d63456c259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e066b97735aa053984bcefaf7a5d6f12a223ae80c42577a9eb22d18fdfd329f`

```dockerfile
```

-	Layers:
	-	`sha256:4406ecedc062847378d5a2598efc22fb863a53371b83b7ee9777bd78686bb47c`  
		Last Modified: Wed, 04 Dec 2024 07:16:02 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ed98f8d018adfd364fc9d7e2de83f9d917bb84ccfe341a81529e8c75cb1d4983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64229583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3deaa95682da6511fa6663c65f1849955a86ec6ba43f1806bd2fb3d34f0959aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Dec 2024 22:20:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4036cbb7a2e5b8a0ce714e4d08fbb64576b80cdd256ff9f0cba6473d73c3d`  
		Last Modified: Wed, 04 Dec 2024 01:35:25 GMT  
		Size: 8.0 MB (7998285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60d77d28745a9052470e2cbb96a13d33e0a0e02f2499098e3d150ae69df6ec1`  
		Last Modified: Wed, 04 Dec 2024 01:35:24 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91ef372941d329672b67f1838f7226808a97f8e58397715e78cd330e0868a9`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd17f2da053085769cb4bd5050acf30ee866b24423db4f6a4501542ff3c577e`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.1 MB (17094301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bf40ee41c170bda856abc36f41024d06b357a9952ada38b13eaa38f5e4fb42`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17533136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28d3c43303886712330874ba9a1a16c23148a9c3d9473bf8a713a8daaa7fab`  
		Last Modified: Wed, 04 Dec 2024 01:35:43 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37013ffc205c5864e92c2dcb7e0f270522f1567a8aa872a4387741223a709686`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ffff7c773efbee73c878f22b1180466f0913d6bf9c789fc84e7327463c4b72`  
		Last Modified: Wed, 04 Dec 2024 01:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:89653bb376bb66d9b4285057ac3ef866b1f38f454dc2cf845eea425b256d574a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adff726fa9c26542fdb2a358bed40114b2f49f65c8b15d54a96fe1ea96fbffde`

```dockerfile
```

-	Layers:
	-	`sha256:99a5a481e67b73498a168bb2f8d905ae5cac8c1cac90b1893ecc3e6c2c393d0f`  
		Last Modified: Wed, 04 Dec 2024 01:35:43 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:6ca9a6811085e2cf769cbac04bc47daf66629102990391caab7cf37426e939da
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
$ docker pull docker@sha256:36f7e13d969ec9bffe8d2700da5168c1e1bc69cb1e25dca50bfe9591db4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (135026509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37123e40ec5295ac68158ace2d5c302a8a5d33f6e40b9a3397be063f941d3705`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99c836815720eb35e0ac10baba1a625902fa8619ab24dbacb464e77b5621e4`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 7.9 MB (7889946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441473b54564f25321bb746ad1ece9e72511542e0e2cf2d6c4a685d55642042f`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b67a33361a7355f408f37f39fba74992e5a77bad7adfbfeb50867380ee2058`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db7f9329b5aa8a8e730800809a97cdbd9afc59ceb4e4ecdaf48b1292ef8247e`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.8 MB (18797158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d946c4c96d3bb716e1307d14a988d350554bf9683300d19cb603834ba7f70b43`  
		Last Modified: Wed, 04 Dec 2024 00:29:14 GMT  
		Size: 19.2 MB (19188666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91324bcb958d9893a36d0a635b1b119c08ecf5aeea0c33a8933695c558b1f15`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa70352df20029e281f85627f717681287f1c2ad199e13366e98afddf22ba20`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dc30100905c3dd4f8be02226d67905079d48b660f5131a0bdb9ac5b53ec318`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b7affd2cbd2d63776ef3a56b1e8e87bbe6c4ff45926945f9d0bd59a70fbc8a`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 9.1 MB (9067299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b563b244ec69075f74c96a055589724459ad7cf3e1dd2fe88db465ecf4d906ff`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 89.2 KB (89239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0d3672080b087610cc6e91768c0cf10636fa7f019a0df3ac2a20b3a93344b`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9a91997e3508e37720f5db1be866b04d023f042b900dd7ceac9d60489a8af3`  
		Last Modified: Wed, 04 Dec 2024 01:28:36 GMT  
		Size: 57.8 MB (57798931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efa22532f8b3bec3ec076779c6ad758bc7e8068de8736d2eb0eeb51c20c763d`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78f3fd7b6197e4187d96cdb25a2436872c022b3c665cbad20d48b3abfb9853`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3b16f4d38590b89620d50f77fea6ac71e3e62f7009693ebc9a309dfb104b3942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b187b4999b26b9e4634e31634862a675a485c82687b846ad67d258920d1e5865`

```dockerfile
```

-	Layers:
	-	`sha256:e1fe188fc168b4b977096e6aa2b3e2c91716308c54bcffe967c4e398f8058419`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:bc484346674dbccdad51e302aeba0ac06e9d3650dfaf52a4961515c80f79c5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125903353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe332abc325288026bb27880b82475f8a713e552c7fa06958233fbc392385be`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dec1f3e06da3f8757b7ab0c912b2790b19463c9e38b2e62db7016713ec835a`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 7.8 MB (7820557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42de83cdff8ecb35d376bef426a487ec59cb3c6e47646a152914957e84298f0d`  
		Last Modified: Tue, 12 Nov 2024 02:19:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7e03894c45574eb692f15e4d6931a5483f1332581f7edad8bd3d3aa28078a4`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 16.6 MB (16601553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416b9ce4eadc755f144844cbf118e90f4562ea751a4b3a7d5cbdf3ef493d2a6a`  
		Last Modified: Wed, 04 Dec 2024 00:29:28 GMT  
		Size: 17.4 MB (17446678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f851db5c0708c729bed8901e10a62c5b08c100e328b7e0c98a25452f22134533`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 18.0 MB (18000429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6022bb89098191f5e257aa4e32bcfa33c5ad77af1820164d53a2d23a155c1efb`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e5a5238bf0b1dc3a4eee05c5847d1c25e2d05a3872672ff9030a6e39564f2`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e341b6cbf0b1d0892b191cafb94e2bb674ea7086b15fb46fddcfc0a87a0950`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37118131d8c6abc8a1d2bc3d06b19e716aba85bd70ef596e731912b3263caf68`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 9.1 MB (9060142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808ad8667e97e661f5dbf6ef2725dc1e89602f0c51f25e110c1d5d182a490c6`  
		Last Modified: Wed, 04 Dec 2024 01:28:49 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11440987ff8e3e813048fee3b7b704ec574022260dbe66591f9cd4b8c43dcd9c`  
		Last Modified: Wed, 04 Dec 2024 01:28:49 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c7b913e1f09d88e471b3909933b4992191770bb8f0d7987e9407b55d8f4b29`  
		Last Modified: Wed, 04 Dec 2024 01:28:52 GMT  
		Size: 53.5 MB (53511021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad8d0c2d6a8178e298e85ba96d6d2718f7046df88dfd0f2acf48946a20f6f1`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b4367498a260de054f3ab7caa2301f404535c5be8ceb9af00fc820a6d010a8`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0528ca2fa8acf242eac680e7dc3b059e769d47969412203ef9b30b692461f64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2eada113d5f4c8076d65858800c094e7761c0da275e0aeecccb35c15a583d83`

```dockerfile
```

-	Layers:
	-	`sha256:748bd2a8690fba2669cd29c9ba34cb8e69cbb5c5ca2a9e7b12ff0f0209d19674`  
		Last Modified: Wed, 04 Dec 2024 01:28:48 GMT  
		Size: 34.7 KB (34730 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:4282a706d0de62d1870d0748595012675b214e349123d04f8b28047f95fe7bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124083382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cd6b3959c6bdcfe0c15f185deaad456030912d24466023e92da5839f19c077`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a8d373266083cffcbf2a6623223d8b2c780180ffc25c641834fa0f399b861c`  
		Last Modified: Wed, 04 Dec 2024 07:15:41 GMT  
		Size: 7.2 MB (7153539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ecea7f1649dbef369192500f3eda21b1f30ba448ca4b382f6dc90ba4b77ed6`  
		Last Modified: Wed, 04 Dec 2024 07:15:40 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8345cbaadf649b7179d374408307a49de91dcad20d33264ff67e18f1df31ad`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 16.6 MB (16591541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0a479bcd6279df331f32a4aab4c0c1f2140ff8ad6863ac2e92df68745f4212`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 17.4 MB (17426318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bda8e0c337df3901bcac5c617da87c4374d34e45d2442c84e52a57079226`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 18.0 MB (17984726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922d604be17f4bbd00d6ed640b5b13212bb106fd9e1de0c22b96b23de6b53f8f`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f87b589e7a688691cd8e51d42d71f370527d4b4710084733eb6d3a885f95c8`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dbeec76024b177d0212c7c8e652f88917461283d8538caf5e1b7120885f229`  
		Last Modified: Wed, 04 Dec 2024 07:16:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87469764160593846c30c8e28dac1080459b4051932d74fd34db73c0027d0565`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 8.2 MB (8228295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba34f50361e4b02b179eb03250dade6609581cc47552001b3b992c82798031d`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 84.5 KB (84498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a38bc738f51a41a50f63665a4183c459cf953d52052327d82e14c4fc2d069a`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38510939bc5659853d67592adbfba6d41d4f83a34c086b45ca197351df04db42`  
		Last Modified: Wed, 04 Dec 2024 09:58:59 GMT  
		Size: 53.5 MB (53511037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca93ad33ff91f6aaf58315b3c74581ce07d1f79488e6b309946a372f1928266`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cf7c178aa1938ea5f4c2b273d58b83721fe1c7133e13e05e37da3dd1b36839`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5060a914795d4ad7da1ec0b4baaa83c418aed4aa32a77f3269faa0676cf4ef54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56e35531d708cdb1857fb999b927304860627396f593f2f6bc9a5f8d9940760`

```dockerfile
```

-	Layers:
	-	`sha256:dda6401da3e01b40934462451eae7cf3f9e919ee3b1f51514bdb8af45a26d9dc`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 34.7 KB (34730 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4d045d01ee7e2c931e74d17300e3e1994aa561841fc20f2323c64f36dcb6b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127617087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa4bd8f7eb76767555fa9b4fcfad991cb6ce4d97f38b7f5d83778b35ca10143`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4036cbb7a2e5b8a0ce714e4d08fbb64576b80cdd256ff9f0cba6473d73c3d`  
		Last Modified: Wed, 04 Dec 2024 01:35:25 GMT  
		Size: 8.0 MB (7998285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60d77d28745a9052470e2cbb96a13d33e0a0e02f2499098e3d150ae69df6ec1`  
		Last Modified: Wed, 04 Dec 2024 01:35:24 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91ef372941d329672b67f1838f7226808a97f8e58397715e78cd330e0868a9`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd17f2da053085769cb4bd5050acf30ee866b24423db4f6a4501542ff3c577e`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.1 MB (17094301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bf40ee41c170bda856abc36f41024d06b357a9952ada38b13eaa38f5e4fb42`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17533136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28d3c43303886712330874ba9a1a16c23148a9c3d9473bf8a713a8daaa7fab`  
		Last Modified: Wed, 04 Dec 2024 01:35:43 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37013ffc205c5864e92c2dcb7e0f270522f1567a8aa872a4387741223a709686`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ffff7c773efbee73c878f22b1180466f0913d6bf9c789fc84e7327463c4b72`  
		Last Modified: Wed, 04 Dec 2024 01:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91e6f6ccb3fb7cbb88f239f42c64aada23404c0c4dce018a70293397b6a7bb2`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 9.9 MB (9854884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b149a083ef4ec99e387305c4f67b50322dca8423ae3768a35f45a2fd271e4f`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 98.7 KB (98661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ba97446cb2349c7c7ede5bac8c57eb62af7c4ed374b72d5c63231122fd3f3e`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c66d82acbf0c58afe05ed4bd7a0e5537ad2a7247cc27a922ca66d5aa62748`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487d2d57a72d0f05061f16b8670991e34849ece621911b2e3501cab1ed7f5ea9`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86120177f87d9b796dce95a7af9473e7763db7ce5380f3ef778d258d244a6c3d`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:53bbd101f17d09cd1cfbce5f9d4ae4d10faf7dea03558020c7bc7b0841655918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239273cc8f9eddd75eaf9bb9f6385ed96d3efeb918b400d9f49b8566fa417e8d`

```dockerfile
```

-	Layers:
	-	`sha256:e8f2b79a35f2afff1c0161dc8445fc1323b9a1ee36026f95eebda18988ec71dc`  
		Last Modified: Wed, 04 Dec 2024 05:06:38 GMT  
		Size: 34.8 KB (34790 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:1b2b351fbccf33af38295d43551a13c85920fc8834eb6dd612ab5b29ffbe5f61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:bfeb145b41ffe9ef3556ffc49a24b1a5d6cfeb083ba571c0aad75c35e48fc460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157312706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602d657ff93975007da8900dd16880b8d2f369ed659b7585842f6c5cb2477e41`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99c836815720eb35e0ac10baba1a625902fa8619ab24dbacb464e77b5621e4`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 7.9 MB (7889946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441473b54564f25321bb746ad1ece9e72511542e0e2cf2d6c4a685d55642042f`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b67a33361a7355f408f37f39fba74992e5a77bad7adfbfeb50867380ee2058`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db7f9329b5aa8a8e730800809a97cdbd9afc59ceb4e4ecdaf48b1292ef8247e`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.8 MB (18797158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d946c4c96d3bb716e1307d14a988d350554bf9683300d19cb603834ba7f70b43`  
		Last Modified: Wed, 04 Dec 2024 00:29:14 GMT  
		Size: 19.2 MB (19188666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91324bcb958d9893a36d0a635b1b119c08ecf5aeea0c33a8933695c558b1f15`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa70352df20029e281f85627f717681287f1c2ad199e13366e98afddf22ba20`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dc30100905c3dd4f8be02226d67905079d48b660f5131a0bdb9ac5b53ec318`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b7affd2cbd2d63776ef3a56b1e8e87bbe6c4ff45926945f9d0bd59a70fbc8a`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 9.1 MB (9067299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b563b244ec69075f74c96a055589724459ad7cf3e1dd2fe88db465ecf4d906ff`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 89.2 KB (89239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0d3672080b087610cc6e91768c0cf10636fa7f019a0df3ac2a20b3a93344b`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9a91997e3508e37720f5db1be866b04d023f042b900dd7ceac9d60489a8af3`  
		Last Modified: Wed, 04 Dec 2024 01:28:36 GMT  
		Size: 57.8 MB (57798931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efa22532f8b3bec3ec076779c6ad758bc7e8068de8736d2eb0eeb51c20c763d`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78f3fd7b6197e4187d96cdb25a2436872c022b3c665cbad20d48b3abfb9853`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd727647cf166fa61ed321eb0608c2ed893d10c8c4b09ee2a806d0259bbaa50`  
		Last Modified: Wed, 04 Dec 2024 02:08:00 GMT  
		Size: 981.6 KB (981585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1388c3a7e6a544063351fba798dd4389ddb866a5cb093523ac8241a780d0b`  
		Last Modified: Wed, 04 Dec 2024 02:08:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8cf5a6f965e7604fa038692249aaacf2ef59bf47d6d93184ea16c7c7367ab3`  
		Last Modified: Wed, 04 Dec 2024 02:08:00 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49cb488e6c4d489302455ac39d4d971d32426c5916518d413b804209eac932e`  
		Last Modified: Wed, 04 Dec 2024 02:08:00 GMT  
		Size: 21.3 MB (21303257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd5c42312c565b90deeed088c484bb72baf226782654bb7682d0551e5dd99b`  
		Last Modified: Wed, 04 Dec 2024 02:08:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b18dae6fe7ca01fa7f257664f27a336ecb5b07f6892966bbc273d7c79787af70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e01492ac0d29b6810facbbeea0ad243c51aa3f4257c8111a2eef625c99f905`

```dockerfile
```

-	Layers:
	-	`sha256:cabdaea5e1d1cfe7eadde7650768cf938a0ca9a6bf654b014adc41960eae8205`  
		Last Modified: Wed, 04 Dec 2024 02:08:00 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:82a231f94a5c3eec69ddf54239ae1d41169fdf355d80b8e328d5938e8326f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151797721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ab80105b16794b12aecca705a72a96bdbf698f53e2b3f6e8f4d0114a22781c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4036cbb7a2e5b8a0ce714e4d08fbb64576b80cdd256ff9f0cba6473d73c3d`  
		Last Modified: Wed, 04 Dec 2024 01:35:25 GMT  
		Size: 8.0 MB (7998285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60d77d28745a9052470e2cbb96a13d33e0a0e02f2499098e3d150ae69df6ec1`  
		Last Modified: Wed, 04 Dec 2024 01:35:24 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91ef372941d329672b67f1838f7226808a97f8e58397715e78cd330e0868a9`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd17f2da053085769cb4bd5050acf30ee866b24423db4f6a4501542ff3c577e`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.1 MB (17094301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bf40ee41c170bda856abc36f41024d06b357a9952ada38b13eaa38f5e4fb42`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17533136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28d3c43303886712330874ba9a1a16c23148a9c3d9473bf8a713a8daaa7fab`  
		Last Modified: Wed, 04 Dec 2024 01:35:43 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37013ffc205c5864e92c2dcb7e0f270522f1567a8aa872a4387741223a709686`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ffff7c773efbee73c878f22b1180466f0913d6bf9c789fc84e7327463c4b72`  
		Last Modified: Wed, 04 Dec 2024 01:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91e6f6ccb3fb7cbb88f239f42c64aada23404c0c4dce018a70293397b6a7bb2`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 9.9 MB (9854884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b149a083ef4ec99e387305c4f67b50322dca8423ae3768a35f45a2fd271e4f`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 98.7 KB (98661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ba97446cb2349c7c7ede5bac8c57eb62af7c4ed374b72d5c63231122fd3f3e`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c66d82acbf0c58afe05ed4bd7a0e5537ad2a7247cc27a922ca66d5aa62748`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487d2d57a72d0f05061f16b8670991e34849ece621911b2e3501cab1ed7f5ea9`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86120177f87d9b796dce95a7af9473e7763db7ce5380f3ef778d258d244a6c3d`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b68388ee45f4cf36e871fa6b36fe6562b0229cd12c393eaf7b1f91999a096`  
		Last Modified: Wed, 04 Dec 2024 06:07:23 GMT  
		Size: 1.0 MB (1023835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaebb36a0d321fb4e524ccd00f7dc8d77e1af96af297fda340b0fc4697c8dceb`  
		Last Modified: Wed, 04 Dec 2024 06:07:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5309cd944cfbb9545e19804cf14a7047c0d037e964b4af777ad90db402439090`  
		Last Modified: Wed, 04 Dec 2024 06:07:23 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767f20920accfd5b334a0c48f65a7fbaeeabdbb6226fc8dec097bac07f6d62a`  
		Last Modified: Wed, 04 Dec 2024 06:07:24 GMT  
		Size: 23.2 MB (23155444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4fa73f9752a24ca5144df670f8cb218b162efcfc0be491a4eb2c4f46037e32`  
		Last Modified: Wed, 04 Dec 2024 06:07:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:639bb7a097dd9e2d08ab61a637a2ae691431bb4e0ed5c63257baca1c9f68751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9153f6539bcf68c449e2894dd61cc51c3ca7013538bc81de0d0a5bf566a305ed`

```dockerfile
```

-	Layers:
	-	`sha256:659863110b37ff1add0d73fd6e3bb2e0a0974b3cd4f46ae5bd68ffd4100a047f`  
		Last Modified: Wed, 04 Dec 2024 06:07:23 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:a9b533ad3897a104820d026bf803f1961f7a5878421714a612247124d0acef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull docker@sha256:8f9c48d09df59573b09228e9dbfe3c594742424cae7426a5a35e8cc7aa3b36c4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311481903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97457ae6f523445fb75426553bfe303fced59f9220ae078d7e4c87715d45fc5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 04 Dec 2024 00:29:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Dec 2024 00:29:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Dec 2024 00:29:23 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 04 Dec 2024 00:29:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 04 Dec 2024 00:29:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:29:33 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 00:29:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Wed, 04 Dec 2024 00:29:34 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Wed, 04 Dec 2024 00:29:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:29:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 00:29:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 04 Dec 2024 00:29:45 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 04 Dec 2024 00:29:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8cf801ea0b73e0642e0b4ce32164423c74578a15913ce3c1522455550a51dc`  
		Last Modified: Wed, 04 Dec 2024 00:30:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce32181c8d548c5f3d5c7f21d6c1b4c138f11930d3b7148aca72a20670d60ef8`  
		Last Modified: Wed, 04 Dec 2024 00:30:02 GMT  
		Size: 368.7 KB (368664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6383050bfd01e5a60b58e3afe6ec6d1727c6c572e4ae362fb203f6547a3d36ba`  
		Last Modified: Wed, 04 Dec 2024 00:30:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3b0dbd135c9afcb2d3a67cf6793d6b0105763d826d910b5be9f56306cf0699`  
		Last Modified: Wed, 04 Dec 2024 00:30:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b486b2b85df328dd041bb776e8189405348f40be4026b361979170287dbf83`  
		Last Modified: Wed, 04 Dec 2024 00:30:04 GMT  
		Size: 18.9 MB (18895345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a797eeea5ccf96cfa615e788b8c83761178eaec7b197ce58af1f7617f1f47bf1`  
		Last Modified: Wed, 04 Dec 2024 00:30:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d270eee49201dcbef13d72f80110cf8520fe216813b9dbbd77a7bccb0671cb`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa40b1420cb32241d443d54fcb9c66295fc1614b803dd2b64b85b8045e88f83`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdec4827b0809606345cd494f89179f7a6a4bfa53c66de763707cc7a8a51a69b`  
		Last Modified: Wed, 04 Dec 2024 00:30:00 GMT  
		Size: 19.7 MB (19654760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b138a6306b3265d89ccf4b591674811e587f9f015dc00aa72e46fb90a33a43`  
		Last Modified: Wed, 04 Dec 2024 00:29:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ff6d4acbb626052eaf329cc2b79f40f95d3ea7e6c9dcd9fc0096b1468e0438`  
		Last Modified: Wed, 04 Dec 2024 00:29:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c8eb7eb52107738c2ba26a34591f105b95d2313a00e6000ae6e8f6722398e9`  
		Last Modified: Wed, 04 Dec 2024 00:29:56 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff881f29ea45eed545b1bee34dead2669cdfd435ecee8af251e2c4265367496d`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 20.1 MB (20067322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull docker@sha256:a2f5603c325e20bc846be7390f49f6dd7324812808f488f3e72bc9dde2f96d57
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2069734614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4603a9f3517e481eeec493fb07aa7eb2eeb779ce43cb2e34606b68efb8e8a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 04 Dec 2024 00:29:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Dec 2024 00:29:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Dec 2024 00:29:50 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 04 Dec 2024 00:29:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 04 Dec 2024 00:30:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:07 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 00:30:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Wed, 04 Dec 2024 00:30:08 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Wed, 04 Dec 2024 00:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 00:30:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 04 Dec 2024 00:30:22 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 04 Dec 2024 00:30:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c8c0d9c38caabebe3b73ab4c6eba8436f7f6362870802faa333902e268fda5`  
		Last Modified: Wed, 04 Dec 2024 00:30:42 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2a635d22c65bd08f6832968bbaf45742dcea846553e69cd5fb73524892186`  
		Last Modified: Wed, 04 Dec 2024 00:30:42 GMT  
		Size: 488.7 KB (488667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec026becc11bd18a346a2f61ef141260e67d4d5c5275e554a9668f99a60e2696`  
		Last Modified: Wed, 04 Dec 2024 00:30:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437214d0ea2a048e24dd206aecfeccb6ce5ccb823890b1ca8feb925dda2c9dd`  
		Last Modified: Wed, 04 Dec 2024 00:30:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4425edecd3624e76b516e6a14bf2381a3228b5b0cd0ca91f5b52242f0b761f52`  
		Last Modified: Wed, 04 Dec 2024 00:30:43 GMT  
		Size: 18.9 MB (18886052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8c997f46007664e2420e190bd026b2d3c615f2f092e4db109bcb66fbc2c230`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b692b1d417f77186832f783e691e3886c3b8473566614323f8090f22aaf482ef`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb109cfc2d9438feb076d8b232441c406096b2b98b39bdc3d6c8b71cff4a6f8f`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76412645838ed469d125fe7cbb4ee913c5e077868700d13338ed009778d34bb4`  
		Last Modified: Wed, 04 Dec 2024 00:30:40 GMT  
		Size: 19.6 MB (19644914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4314d510cc852d692dd9c73cb48da4c06607bf2426a12a710a1f7f23168cf6a8`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e08b405dd71ce49510066489c12e9c6d278bb87ddfce055c2ea7a51a7a1ea67`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61005e57942a2a801aafe59b869523568ec1b842f394fd1d5881b321422de2`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627830bfad7c6a2e11305e97939175b7844471db27f68b649091073c61f7f394`  
		Last Modified: Wed, 04 Dec 2024 00:30:40 GMT  
		Size: 20.0 MB (20049522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:f06d2055c2e10f622d21e2227032bf6ecba6d0b6444ba17059b7e4c822a3c9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull docker@sha256:a2f5603c325e20bc846be7390f49f6dd7324812808f488f3e72bc9dde2f96d57
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2069734614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4603a9f3517e481eeec493fb07aa7eb2eeb779ce43cb2e34606b68efb8e8a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 04 Dec 2024 00:29:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Dec 2024 00:29:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Dec 2024 00:29:50 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 04 Dec 2024 00:29:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 04 Dec 2024 00:30:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:07 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 00:30:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Wed, 04 Dec 2024 00:30:08 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Wed, 04 Dec 2024 00:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 00:30:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 04 Dec 2024 00:30:22 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 04 Dec 2024 00:30:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c8c0d9c38caabebe3b73ab4c6eba8436f7f6362870802faa333902e268fda5`  
		Last Modified: Wed, 04 Dec 2024 00:30:42 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2a635d22c65bd08f6832968bbaf45742dcea846553e69cd5fb73524892186`  
		Last Modified: Wed, 04 Dec 2024 00:30:42 GMT  
		Size: 488.7 KB (488667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec026becc11bd18a346a2f61ef141260e67d4d5c5275e554a9668f99a60e2696`  
		Last Modified: Wed, 04 Dec 2024 00:30:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437214d0ea2a048e24dd206aecfeccb6ce5ccb823890b1ca8feb925dda2c9dd`  
		Last Modified: Wed, 04 Dec 2024 00:30:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4425edecd3624e76b516e6a14bf2381a3228b5b0cd0ca91f5b52242f0b761f52`  
		Last Modified: Wed, 04 Dec 2024 00:30:43 GMT  
		Size: 18.9 MB (18886052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8c997f46007664e2420e190bd026b2d3c615f2f092e4db109bcb66fbc2c230`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b692b1d417f77186832f783e691e3886c3b8473566614323f8090f22aaf482ef`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb109cfc2d9438feb076d8b232441c406096b2b98b39bdc3d6c8b71cff4a6f8f`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76412645838ed469d125fe7cbb4ee913c5e077868700d13338ed009778d34bb4`  
		Last Modified: Wed, 04 Dec 2024 00:30:40 GMT  
		Size: 19.6 MB (19644914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4314d510cc852d692dd9c73cb48da4c06607bf2426a12a710a1f7f23168cf6a8`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e08b405dd71ce49510066489c12e9c6d278bb87ddfce055c2ea7a51a7a1ea67`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61005e57942a2a801aafe59b869523568ec1b842f394fd1d5881b321422de2`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627830bfad7c6a2e11305e97939175b7844471db27f68b649091073c61f7f394`  
		Last Modified: Wed, 04 Dec 2024 00:30:40 GMT  
		Size: 20.0 MB (20049522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9660f39af1699dd42956f5c43ab9d1f0e7229bbfce8129b52fa0cd9fde98d042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull docker@sha256:8f9c48d09df59573b09228e9dbfe3c594742424cae7426a5a35e8cc7aa3b36c4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311481903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97457ae6f523445fb75426553bfe303fced59f9220ae078d7e4c87715d45fc5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 04 Dec 2024 00:29:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Dec 2024 00:29:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Dec 2024 00:29:23 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 04 Dec 2024 00:29:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 04 Dec 2024 00:29:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:29:33 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 00:29:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Wed, 04 Dec 2024 00:29:34 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Wed, 04 Dec 2024 00:29:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:29:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 00:29:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 04 Dec 2024 00:29:45 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 04 Dec 2024 00:29:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8cf801ea0b73e0642e0b4ce32164423c74578a15913ce3c1522455550a51dc`  
		Last Modified: Wed, 04 Dec 2024 00:30:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce32181c8d548c5f3d5c7f21d6c1b4c138f11930d3b7148aca72a20670d60ef8`  
		Last Modified: Wed, 04 Dec 2024 00:30:02 GMT  
		Size: 368.7 KB (368664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6383050bfd01e5a60b58e3afe6ec6d1727c6c572e4ae362fb203f6547a3d36ba`  
		Last Modified: Wed, 04 Dec 2024 00:30:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3b0dbd135c9afcb2d3a67cf6793d6b0105763d826d910b5be9f56306cf0699`  
		Last Modified: Wed, 04 Dec 2024 00:30:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b486b2b85df328dd041bb776e8189405348f40be4026b361979170287dbf83`  
		Last Modified: Wed, 04 Dec 2024 00:30:04 GMT  
		Size: 18.9 MB (18895345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a797eeea5ccf96cfa615e788b8c83761178eaec7b197ce58af1f7617f1f47bf1`  
		Last Modified: Wed, 04 Dec 2024 00:30:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d270eee49201dcbef13d72f80110cf8520fe216813b9dbbd77a7bccb0671cb`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa40b1420cb32241d443d54fcb9c66295fc1614b803dd2b64b85b8045e88f83`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdec4827b0809606345cd494f89179f7a6a4bfa53c66de763707cc7a8a51a69b`  
		Last Modified: Wed, 04 Dec 2024 00:30:00 GMT  
		Size: 19.7 MB (19654760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b138a6306b3265d89ccf4b591674811e587f9f015dc00aa72e46fb90a33a43`  
		Last Modified: Wed, 04 Dec 2024 00:29:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ff6d4acbb626052eaf329cc2b79f40f95d3ea7e6c9dcd9fc0096b1468e0438`  
		Last Modified: Wed, 04 Dec 2024 00:29:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c8eb7eb52107738c2ba26a34591f105b95d2313a00e6000ae6e8f6722398e9`  
		Last Modified: Wed, 04 Dec 2024 00:29:56 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff881f29ea45eed545b1bee34dead2669cdfd435ecee8af251e2c4265367496d`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 20.1 MB (20067322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.4`

**does not exist** (yet?)

## `docker:27.4-cli`

**does not exist** (yet?)

## `docker:27.4-dind`

**does not exist** (yet?)

## `docker:27.4-dind-rootless`

**does not exist** (yet?)

## `docker:27.4-windowsservercore`

**does not exist** (yet?)

## `docker:27.4-windowsservercore-1809`

**does not exist** (yet?)

## `docker:27.4-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:27.4.0`

**does not exist** (yet?)

## `docker:27.4.0-alpine3.21`

**does not exist** (yet?)

## `docker:27.4.0-cli`

**does not exist** (yet?)

## `docker:27.4.0-cli-alpine3.21`

**does not exist** (yet?)

## `docker:27.4.0-dind`

**does not exist** (yet?)

## `docker:27.4.0-dind-alpine3.21`

**does not exist** (yet?)

## `docker:27.4.0-dind-rootless`

**does not exist** (yet?)

## `docker:27.4.0-windowsservercore`

**does not exist** (yet?)

## `docker:27.4.0-windowsservercore-1809`

**does not exist** (yet?)

## `docker:27.4.0-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:cli`

```console
$ docker pull docker@sha256:328eb399a065780c2cebe9224de003aa14084cf69efae882ac27430f921819b7
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
$ docker pull docker@sha256:f2fb6f02004bd10aaa1b489d19e68f3225aa55c93ad296d322be523911b8664a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68065244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f761a0f3cfe5fb6c1318ed49c84bbb30ba0dd1d7a9c7a619329147cf025b0c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Dec 2024 22:20:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99c836815720eb35e0ac10baba1a625902fa8619ab24dbacb464e77b5621e4`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 7.9 MB (7889946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441473b54564f25321bb746ad1ece9e72511542e0e2cf2d6c4a685d55642042f`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b67a33361a7355f408f37f39fba74992e5a77bad7adfbfeb50867380ee2058`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db7f9329b5aa8a8e730800809a97cdbd9afc59ceb4e4ecdaf48b1292ef8247e`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.8 MB (18797158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d946c4c96d3bb716e1307d14a988d350554bf9683300d19cb603834ba7f70b43`  
		Last Modified: Wed, 04 Dec 2024 00:29:14 GMT  
		Size: 19.2 MB (19188666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91324bcb958d9893a36d0a635b1b119c08ecf5aeea0c33a8933695c558b1f15`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa70352df20029e281f85627f717681287f1c2ad199e13366e98afddf22ba20`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dc30100905c3dd4f8be02226d67905079d48b660f5131a0bdb9ac5b53ec318`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:28b2a9a1c41faefd01e667161876764eb1585c01198ce6a9fadf02876114084e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5fbbd12270145b2fe25952cd19c6f7dadaf0bbb16a703a91da3c67c77f52fe`

```dockerfile
```

-	Layers:
	-	`sha256:0ef8d39d9caf19a29683d5f428c541269a025b580dc6c79972ca68cc0abb9191`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:bd6b01e7e15db48211c58491f5ab02744ee75b8c72a3c9b3f1ae774c2bfe4fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63237978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5417cde1ea6bf81d248fc4a90c9580aee1e0c8c66dc3e0efe2ccb6754745d999`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Dec 2024 22:20:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dec1f3e06da3f8757b7ab0c912b2790b19463c9e38b2e62db7016713ec835a`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 7.8 MB (7820557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42de83cdff8ecb35d376bef426a487ec59cb3c6e47646a152914957e84298f0d`  
		Last Modified: Tue, 12 Nov 2024 02:19:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7e03894c45574eb692f15e4d6931a5483f1332581f7edad8bd3d3aa28078a4`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 16.6 MB (16601553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416b9ce4eadc755f144844cbf118e90f4562ea751a4b3a7d5cbdf3ef493d2a6a`  
		Last Modified: Wed, 04 Dec 2024 00:29:28 GMT  
		Size: 17.4 MB (17446678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f851db5c0708c729bed8901e10a62c5b08c100e328b7e0c98a25452f22134533`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 18.0 MB (18000429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6022bb89098191f5e257aa4e32bcfa33c5ad77af1820164d53a2d23a155c1efb`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e5a5238bf0b1dc3a4eee05c5847d1c25e2d05a3872672ff9030a6e39564f2`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e341b6cbf0b1d0892b191cafb94e2bb674ea7086b15fb46fddcfc0a87a0950`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:40edb31e4f25fd23bb7a242cef0277168fdb7c2928efad81eccf6b64973ffde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d27ae93b0cb111b4172a77c7836f3898a3d6235cbfdf8a277229f783fa5f4f`

```dockerfile
```

-	Layers:
	-	`sha256:dd6ac4f9bb23336484e3057f20ee57df54cbc347925af0095edfb3c06ba0b7f3`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:e87ad798b53baef6d90b5c44af8303ab6cd0ef49e2abab0729d6f151d8071369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62253760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c8f13ab34b5cb8d9487941ad1be49ff1e82f2564a275b559aeac8aabc4d7f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Dec 2024 22:20:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a8d373266083cffcbf2a6623223d8b2c780180ffc25c641834fa0f399b861c`  
		Last Modified: Wed, 04 Dec 2024 07:15:41 GMT  
		Size: 7.2 MB (7153539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ecea7f1649dbef369192500f3eda21b1f30ba448ca4b382f6dc90ba4b77ed6`  
		Last Modified: Wed, 04 Dec 2024 07:15:40 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8345cbaadf649b7179d374408307a49de91dcad20d33264ff67e18f1df31ad`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 16.6 MB (16591541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0a479bcd6279df331f32a4aab4c0c1f2140ff8ad6863ac2e92df68745f4212`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 17.4 MB (17426318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bda8e0c337df3901bcac5c617da87c4374d34e45d2442c84e52a57079226`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 18.0 MB (17984726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922d604be17f4bbd00d6ed640b5b13212bb106fd9e1de0c22b96b23de6b53f8f`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f87b589e7a688691cd8e51d42d71f370527d4b4710084733eb6d3a885f95c8`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dbeec76024b177d0212c7c8e652f88917461283d8538caf5e1b7120885f229`  
		Last Modified: Wed, 04 Dec 2024 07:16:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a2e1f67dc70fae764b891ca53c791a1e606c473bf557dc90c21957d63456c259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e066b97735aa053984bcefaf7a5d6f12a223ae80c42577a9eb22d18fdfd329f`

```dockerfile
```

-	Layers:
	-	`sha256:4406ecedc062847378d5a2598efc22fb863a53371b83b7ee9777bd78686bb47c`  
		Last Modified: Wed, 04 Dec 2024 07:16:02 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ed98f8d018adfd364fc9d7e2de83f9d917bb84ccfe341a81529e8c75cb1d4983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64229583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3deaa95682da6511fa6663c65f1849955a86ec6ba43f1806bd2fb3d34f0959aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Tue, 03 Dec 2024 22:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Dec 2024 22:20:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Dec 2024 22:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 22:20:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4036cbb7a2e5b8a0ce714e4d08fbb64576b80cdd256ff9f0cba6473d73c3d`  
		Last Modified: Wed, 04 Dec 2024 01:35:25 GMT  
		Size: 8.0 MB (7998285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60d77d28745a9052470e2cbb96a13d33e0a0e02f2499098e3d150ae69df6ec1`  
		Last Modified: Wed, 04 Dec 2024 01:35:24 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91ef372941d329672b67f1838f7226808a97f8e58397715e78cd330e0868a9`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd17f2da053085769cb4bd5050acf30ee866b24423db4f6a4501542ff3c577e`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.1 MB (17094301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bf40ee41c170bda856abc36f41024d06b357a9952ada38b13eaa38f5e4fb42`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17533136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28d3c43303886712330874ba9a1a16c23148a9c3d9473bf8a713a8daaa7fab`  
		Last Modified: Wed, 04 Dec 2024 01:35:43 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37013ffc205c5864e92c2dcb7e0f270522f1567a8aa872a4387741223a709686`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ffff7c773efbee73c878f22b1180466f0913d6bf9c789fc84e7327463c4b72`  
		Last Modified: Wed, 04 Dec 2024 01:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:89653bb376bb66d9b4285057ac3ef866b1f38f454dc2cf845eea425b256d574a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adff726fa9c26542fdb2a358bed40114b2f49f65c8b15d54a96fe1ea96fbffde`

```dockerfile
```

-	Layers:
	-	`sha256:99a5a481e67b73498a168bb2f8d905ae5cac8c1cac90b1893ecc3e6c2c393d0f`  
		Last Modified: Wed, 04 Dec 2024 01:35:43 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:6ca9a6811085e2cf769cbac04bc47daf66629102990391caab7cf37426e939da
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
$ docker pull docker@sha256:36f7e13d969ec9bffe8d2700da5168c1e1bc69cb1e25dca50bfe9591db4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (135026509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37123e40ec5295ac68158ace2d5c302a8a5d33f6e40b9a3397be063f941d3705`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99c836815720eb35e0ac10baba1a625902fa8619ab24dbacb464e77b5621e4`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 7.9 MB (7889946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441473b54564f25321bb746ad1ece9e72511542e0e2cf2d6c4a685d55642042f`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b67a33361a7355f408f37f39fba74992e5a77bad7adfbfeb50867380ee2058`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db7f9329b5aa8a8e730800809a97cdbd9afc59ceb4e4ecdaf48b1292ef8247e`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.8 MB (18797158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d946c4c96d3bb716e1307d14a988d350554bf9683300d19cb603834ba7f70b43`  
		Last Modified: Wed, 04 Dec 2024 00:29:14 GMT  
		Size: 19.2 MB (19188666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91324bcb958d9893a36d0a635b1b119c08ecf5aeea0c33a8933695c558b1f15`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa70352df20029e281f85627f717681287f1c2ad199e13366e98afddf22ba20`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dc30100905c3dd4f8be02226d67905079d48b660f5131a0bdb9ac5b53ec318`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b7affd2cbd2d63776ef3a56b1e8e87bbe6c4ff45926945f9d0bd59a70fbc8a`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 9.1 MB (9067299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b563b244ec69075f74c96a055589724459ad7cf3e1dd2fe88db465ecf4d906ff`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 89.2 KB (89239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0d3672080b087610cc6e91768c0cf10636fa7f019a0df3ac2a20b3a93344b`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9a91997e3508e37720f5db1be866b04d023f042b900dd7ceac9d60489a8af3`  
		Last Modified: Wed, 04 Dec 2024 01:28:36 GMT  
		Size: 57.8 MB (57798931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efa22532f8b3bec3ec076779c6ad758bc7e8068de8736d2eb0eeb51c20c763d`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78f3fd7b6197e4187d96cdb25a2436872c022b3c665cbad20d48b3abfb9853`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:3b16f4d38590b89620d50f77fea6ac71e3e62f7009693ebc9a309dfb104b3942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b187b4999b26b9e4634e31634862a675a485c82687b846ad67d258920d1e5865`

```dockerfile
```

-	Layers:
	-	`sha256:e1fe188fc168b4b977096e6aa2b3e2c91716308c54bcffe967c4e398f8058419`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:bc484346674dbccdad51e302aeba0ac06e9d3650dfaf52a4961515c80f79c5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125903353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe332abc325288026bb27880b82475f8a713e552c7fa06958233fbc392385be`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dec1f3e06da3f8757b7ab0c912b2790b19463c9e38b2e62db7016713ec835a`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 7.8 MB (7820557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42de83cdff8ecb35d376bef426a487ec59cb3c6e47646a152914957e84298f0d`  
		Last Modified: Tue, 12 Nov 2024 02:19:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7e03894c45574eb692f15e4d6931a5483f1332581f7edad8bd3d3aa28078a4`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 16.6 MB (16601553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416b9ce4eadc755f144844cbf118e90f4562ea751a4b3a7d5cbdf3ef493d2a6a`  
		Last Modified: Wed, 04 Dec 2024 00:29:28 GMT  
		Size: 17.4 MB (17446678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f851db5c0708c729bed8901e10a62c5b08c100e328b7e0c98a25452f22134533`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 18.0 MB (18000429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6022bb89098191f5e257aa4e32bcfa33c5ad77af1820164d53a2d23a155c1efb`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e5a5238bf0b1dc3a4eee05c5847d1c25e2d05a3872672ff9030a6e39564f2`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e341b6cbf0b1d0892b191cafb94e2bb674ea7086b15fb46fddcfc0a87a0950`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37118131d8c6abc8a1d2bc3d06b19e716aba85bd70ef596e731912b3263caf68`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 9.1 MB (9060142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808ad8667e97e661f5dbf6ef2725dc1e89602f0c51f25e110c1d5d182a490c6`  
		Last Modified: Wed, 04 Dec 2024 01:28:49 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11440987ff8e3e813048fee3b7b704ec574022260dbe66591f9cd4b8c43dcd9c`  
		Last Modified: Wed, 04 Dec 2024 01:28:49 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c7b913e1f09d88e471b3909933b4992191770bb8f0d7987e9407b55d8f4b29`  
		Last Modified: Wed, 04 Dec 2024 01:28:52 GMT  
		Size: 53.5 MB (53511021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad8d0c2d6a8178e298e85ba96d6d2718f7046df88dfd0f2acf48946a20f6f1`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b4367498a260de054f3ab7caa2301f404535c5be8ceb9af00fc820a6d010a8`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:0528ca2fa8acf242eac680e7dc3b059e769d47969412203ef9b30b692461f64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2eada113d5f4c8076d65858800c094e7761c0da275e0aeecccb35c15a583d83`

```dockerfile
```

-	Layers:
	-	`sha256:748bd2a8690fba2669cd29c9ba34cb8e69cbb5c5ca2a9e7b12ff0f0209d19674`  
		Last Modified: Wed, 04 Dec 2024 01:28:48 GMT  
		Size: 34.7 KB (34730 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:4282a706d0de62d1870d0748595012675b214e349123d04f8b28047f95fe7bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124083382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cd6b3959c6bdcfe0c15f185deaad456030912d24466023e92da5839f19c077`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a8d373266083cffcbf2a6623223d8b2c780180ffc25c641834fa0f399b861c`  
		Last Modified: Wed, 04 Dec 2024 07:15:41 GMT  
		Size: 7.2 MB (7153539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ecea7f1649dbef369192500f3eda21b1f30ba448ca4b382f6dc90ba4b77ed6`  
		Last Modified: Wed, 04 Dec 2024 07:15:40 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8345cbaadf649b7179d374408307a49de91dcad20d33264ff67e18f1df31ad`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 16.6 MB (16591541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0a479bcd6279df331f32a4aab4c0c1f2140ff8ad6863ac2e92df68745f4212`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 17.4 MB (17426318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bda8e0c337df3901bcac5c617da87c4374d34e45d2442c84e52a57079226`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 18.0 MB (17984726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922d604be17f4bbd00d6ed640b5b13212bb106fd9e1de0c22b96b23de6b53f8f`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f87b589e7a688691cd8e51d42d71f370527d4b4710084733eb6d3a885f95c8`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dbeec76024b177d0212c7c8e652f88917461283d8538caf5e1b7120885f229`  
		Last Modified: Wed, 04 Dec 2024 07:16:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87469764160593846c30c8e28dac1080459b4051932d74fd34db73c0027d0565`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 8.2 MB (8228295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba34f50361e4b02b179eb03250dade6609581cc47552001b3b992c82798031d`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 84.5 KB (84498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a38bc738f51a41a50f63665a4183c459cf953d52052327d82e14c4fc2d069a`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38510939bc5659853d67592adbfba6d41d4f83a34c086b45ca197351df04db42`  
		Last Modified: Wed, 04 Dec 2024 09:58:59 GMT  
		Size: 53.5 MB (53511037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca93ad33ff91f6aaf58315b3c74581ce07d1f79488e6b309946a372f1928266`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cf7c178aa1938ea5f4c2b273d58b83721fe1c7133e13e05e37da3dd1b36839`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:5060a914795d4ad7da1ec0b4baaa83c418aed4aa32a77f3269faa0676cf4ef54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56e35531d708cdb1857fb999b927304860627396f593f2f6bc9a5f8d9940760`

```dockerfile
```

-	Layers:
	-	`sha256:dda6401da3e01b40934462451eae7cf3f9e919ee3b1f51514bdb8af45a26d9dc`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 34.7 KB (34730 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4d045d01ee7e2c931e74d17300e3e1994aa561841fc20f2323c64f36dcb6b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127617087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa4bd8f7eb76767555fa9b4fcfad991cb6ce4d97f38b7f5d83778b35ca10143`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4036cbb7a2e5b8a0ce714e4d08fbb64576b80cdd256ff9f0cba6473d73c3d`  
		Last Modified: Wed, 04 Dec 2024 01:35:25 GMT  
		Size: 8.0 MB (7998285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60d77d28745a9052470e2cbb96a13d33e0a0e02f2499098e3d150ae69df6ec1`  
		Last Modified: Wed, 04 Dec 2024 01:35:24 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91ef372941d329672b67f1838f7226808a97f8e58397715e78cd330e0868a9`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd17f2da053085769cb4bd5050acf30ee866b24423db4f6a4501542ff3c577e`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.1 MB (17094301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bf40ee41c170bda856abc36f41024d06b357a9952ada38b13eaa38f5e4fb42`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17533136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28d3c43303886712330874ba9a1a16c23148a9c3d9473bf8a713a8daaa7fab`  
		Last Modified: Wed, 04 Dec 2024 01:35:43 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37013ffc205c5864e92c2dcb7e0f270522f1567a8aa872a4387741223a709686`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ffff7c773efbee73c878f22b1180466f0913d6bf9c789fc84e7327463c4b72`  
		Last Modified: Wed, 04 Dec 2024 01:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91e6f6ccb3fb7cbb88f239f42c64aada23404c0c4dce018a70293397b6a7bb2`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 9.9 MB (9854884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b149a083ef4ec99e387305c4f67b50322dca8423ae3768a35f45a2fd271e4f`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 98.7 KB (98661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ba97446cb2349c7c7ede5bac8c57eb62af7c4ed374b72d5c63231122fd3f3e`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c66d82acbf0c58afe05ed4bd7a0e5537ad2a7247cc27a922ca66d5aa62748`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487d2d57a72d0f05061f16b8670991e34849ece621911b2e3501cab1ed7f5ea9`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86120177f87d9b796dce95a7af9473e7763db7ce5380f3ef778d258d244a6c3d`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:53bbd101f17d09cd1cfbce5f9d4ae4d10faf7dea03558020c7bc7b0841655918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239273cc8f9eddd75eaf9bb9f6385ed96d3efeb918b400d9f49b8566fa417e8d`

```dockerfile
```

-	Layers:
	-	`sha256:e8f2b79a35f2afff1c0161dc8445fc1323b9a1ee36026f95eebda18988ec71dc`  
		Last Modified: Wed, 04 Dec 2024 05:06:38 GMT  
		Size: 34.8 KB (34790 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:1b2b351fbccf33af38295d43551a13c85920fc8834eb6dd612ab5b29ffbe5f61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:bfeb145b41ffe9ef3556ffc49a24b1a5d6cfeb083ba571c0aad75c35e48fc460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157312706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602d657ff93975007da8900dd16880b8d2f369ed659b7585842f6c5cb2477e41`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99c836815720eb35e0ac10baba1a625902fa8619ab24dbacb464e77b5621e4`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 7.9 MB (7889946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441473b54564f25321bb746ad1ece9e72511542e0e2cf2d6c4a685d55642042f`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b67a33361a7355f408f37f39fba74992e5a77bad7adfbfeb50867380ee2058`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db7f9329b5aa8a8e730800809a97cdbd9afc59ceb4e4ecdaf48b1292ef8247e`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.8 MB (18797158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d946c4c96d3bb716e1307d14a988d350554bf9683300d19cb603834ba7f70b43`  
		Last Modified: Wed, 04 Dec 2024 00:29:14 GMT  
		Size: 19.2 MB (19188666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91324bcb958d9893a36d0a635b1b119c08ecf5aeea0c33a8933695c558b1f15`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa70352df20029e281f85627f717681287f1c2ad199e13366e98afddf22ba20`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dc30100905c3dd4f8be02226d67905079d48b660f5131a0bdb9ac5b53ec318`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b7affd2cbd2d63776ef3a56b1e8e87bbe6c4ff45926945f9d0bd59a70fbc8a`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 9.1 MB (9067299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b563b244ec69075f74c96a055589724459ad7cf3e1dd2fe88db465ecf4d906ff`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 89.2 KB (89239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0d3672080b087610cc6e91768c0cf10636fa7f019a0df3ac2a20b3a93344b`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9a91997e3508e37720f5db1be866b04d023f042b900dd7ceac9d60489a8af3`  
		Last Modified: Wed, 04 Dec 2024 01:28:36 GMT  
		Size: 57.8 MB (57798931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efa22532f8b3bec3ec076779c6ad758bc7e8068de8736d2eb0eeb51c20c763d`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78f3fd7b6197e4187d96cdb25a2436872c022b3c665cbad20d48b3abfb9853`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd727647cf166fa61ed321eb0608c2ed893d10c8c4b09ee2a806d0259bbaa50`  
		Last Modified: Wed, 04 Dec 2024 02:08:00 GMT  
		Size: 981.6 KB (981585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1388c3a7e6a544063351fba798dd4389ddb866a5cb093523ac8241a780d0b`  
		Last Modified: Wed, 04 Dec 2024 02:08:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8cf5a6f965e7604fa038692249aaacf2ef59bf47d6d93184ea16c7c7367ab3`  
		Last Modified: Wed, 04 Dec 2024 02:08:00 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49cb488e6c4d489302455ac39d4d971d32426c5916518d413b804209eac932e`  
		Last Modified: Wed, 04 Dec 2024 02:08:00 GMT  
		Size: 21.3 MB (21303257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd5c42312c565b90deeed088c484bb72baf226782654bb7682d0551e5dd99b`  
		Last Modified: Wed, 04 Dec 2024 02:08:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b18dae6fe7ca01fa7f257664f27a336ecb5b07f6892966bbc273d7c79787af70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e01492ac0d29b6810facbbeea0ad243c51aa3f4257c8111a2eef625c99f905`

```dockerfile
```

-	Layers:
	-	`sha256:cabdaea5e1d1cfe7eadde7650768cf938a0ca9a6bf654b014adc41960eae8205`  
		Last Modified: Wed, 04 Dec 2024 02:08:00 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:82a231f94a5c3eec69ddf54239ae1d41169fdf355d80b8e328d5938e8326f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151797721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ab80105b16794b12aecca705a72a96bdbf698f53e2b3f6e8f4d0114a22781c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4036cbb7a2e5b8a0ce714e4d08fbb64576b80cdd256ff9f0cba6473d73c3d`  
		Last Modified: Wed, 04 Dec 2024 01:35:25 GMT  
		Size: 8.0 MB (7998285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60d77d28745a9052470e2cbb96a13d33e0a0e02f2499098e3d150ae69df6ec1`  
		Last Modified: Wed, 04 Dec 2024 01:35:24 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91ef372941d329672b67f1838f7226808a97f8e58397715e78cd330e0868a9`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd17f2da053085769cb4bd5050acf30ee866b24423db4f6a4501542ff3c577e`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.1 MB (17094301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bf40ee41c170bda856abc36f41024d06b357a9952ada38b13eaa38f5e4fb42`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17533136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28d3c43303886712330874ba9a1a16c23148a9c3d9473bf8a713a8daaa7fab`  
		Last Modified: Wed, 04 Dec 2024 01:35:43 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37013ffc205c5864e92c2dcb7e0f270522f1567a8aa872a4387741223a709686`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ffff7c773efbee73c878f22b1180466f0913d6bf9c789fc84e7327463c4b72`  
		Last Modified: Wed, 04 Dec 2024 01:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91e6f6ccb3fb7cbb88f239f42c64aada23404c0c4dce018a70293397b6a7bb2`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 9.9 MB (9854884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b149a083ef4ec99e387305c4f67b50322dca8423ae3768a35f45a2fd271e4f`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 98.7 KB (98661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ba97446cb2349c7c7ede5bac8c57eb62af7c4ed374b72d5c63231122fd3f3e`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c66d82acbf0c58afe05ed4bd7a0e5537ad2a7247cc27a922ca66d5aa62748`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487d2d57a72d0f05061f16b8670991e34849ece621911b2e3501cab1ed7f5ea9`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86120177f87d9b796dce95a7af9473e7763db7ce5380f3ef778d258d244a6c3d`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b68388ee45f4cf36e871fa6b36fe6562b0229cd12c393eaf7b1f91999a096`  
		Last Modified: Wed, 04 Dec 2024 06:07:23 GMT  
		Size: 1.0 MB (1023835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaebb36a0d321fb4e524ccd00f7dc8d77e1af96af297fda340b0fc4697c8dceb`  
		Last Modified: Wed, 04 Dec 2024 06:07:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5309cd944cfbb9545e19804cf14a7047c0d037e964b4af777ad90db402439090`  
		Last Modified: Wed, 04 Dec 2024 06:07:23 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767f20920accfd5b334a0c48f65a7fbaeeabdbb6226fc8dec097bac07f6d62a`  
		Last Modified: Wed, 04 Dec 2024 06:07:24 GMT  
		Size: 23.2 MB (23155444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4fa73f9752a24ca5144df670f8cb218b162efcfc0be491a4eb2c4f46037e32`  
		Last Modified: Wed, 04 Dec 2024 06:07:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:639bb7a097dd9e2d08ab61a637a2ae691431bb4e0ed5c63257baca1c9f68751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9153f6539bcf68c449e2894dd61cc51c3ca7013538bc81de0d0a5bf566a305ed`

```dockerfile
```

-	Layers:
	-	`sha256:659863110b37ff1add0d73fd6e3bb2e0a0974b3cd4f46ae5bd68ffd4100a047f`  
		Last Modified: Wed, 04 Dec 2024 06:07:23 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:6ca9a6811085e2cf769cbac04bc47daf66629102990391caab7cf37426e939da
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
$ docker pull docker@sha256:36f7e13d969ec9bffe8d2700da5168c1e1bc69cb1e25dca50bfe9591db4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (135026509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37123e40ec5295ac68158ace2d5c302a8a5d33f6e40b9a3397be063f941d3705`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99c836815720eb35e0ac10baba1a625902fa8619ab24dbacb464e77b5621e4`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 7.9 MB (7889946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441473b54564f25321bb746ad1ece9e72511542e0e2cf2d6c4a685d55642042f`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b67a33361a7355f408f37f39fba74992e5a77bad7adfbfeb50867380ee2058`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db7f9329b5aa8a8e730800809a97cdbd9afc59ceb4e4ecdaf48b1292ef8247e`  
		Last Modified: Wed, 04 Dec 2024 00:29:12 GMT  
		Size: 18.8 MB (18797158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d946c4c96d3bb716e1307d14a988d350554bf9683300d19cb603834ba7f70b43`  
		Last Modified: Wed, 04 Dec 2024 00:29:14 GMT  
		Size: 19.2 MB (19188666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91324bcb958d9893a36d0a635b1b119c08ecf5aeea0c33a8933695c558b1f15`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa70352df20029e281f85627f717681287f1c2ad199e13366e98afddf22ba20`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dc30100905c3dd4f8be02226d67905079d48b660f5131a0bdb9ac5b53ec318`  
		Last Modified: Wed, 04 Dec 2024 00:29:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b7affd2cbd2d63776ef3a56b1e8e87bbe6c4ff45926945f9d0bd59a70fbc8a`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 9.1 MB (9067299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b563b244ec69075f74c96a055589724459ad7cf3e1dd2fe88db465ecf4d906ff`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 89.2 KB (89239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0d3672080b087610cc6e91768c0cf10636fa7f019a0df3ac2a20b3a93344b`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9a91997e3508e37720f5db1be866b04d023f042b900dd7ceac9d60489a8af3`  
		Last Modified: Wed, 04 Dec 2024 01:28:36 GMT  
		Size: 57.8 MB (57798931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efa22532f8b3bec3ec076779c6ad758bc7e8068de8736d2eb0eeb51c20c763d`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78f3fd7b6197e4187d96cdb25a2436872c022b3c665cbad20d48b3abfb9853`  
		Last Modified: Wed, 04 Dec 2024 01:28:35 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:3b16f4d38590b89620d50f77fea6ac71e3e62f7009693ebc9a309dfb104b3942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b187b4999b26b9e4634e31634862a675a485c82687b846ad67d258920d1e5865`

```dockerfile
```

-	Layers:
	-	`sha256:e1fe188fc168b4b977096e6aa2b3e2c91716308c54bcffe967c4e398f8058419`  
		Last Modified: Wed, 04 Dec 2024 01:28:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:bc484346674dbccdad51e302aeba0ac06e9d3650dfaf52a4961515c80f79c5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125903353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe332abc325288026bb27880b82475f8a713e552c7fa06958233fbc392385be`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dec1f3e06da3f8757b7ab0c912b2790b19463c9e38b2e62db7016713ec835a`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 7.8 MB (7820557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42de83cdff8ecb35d376bef426a487ec59cb3c6e47646a152914957e84298f0d`  
		Last Modified: Tue, 12 Nov 2024 02:19:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7e03894c45574eb692f15e4d6931a5483f1332581f7edad8bd3d3aa28078a4`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 16.6 MB (16601553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416b9ce4eadc755f144844cbf118e90f4562ea751a4b3a7d5cbdf3ef493d2a6a`  
		Last Modified: Wed, 04 Dec 2024 00:29:28 GMT  
		Size: 17.4 MB (17446678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f851db5c0708c729bed8901e10a62c5b08c100e328b7e0c98a25452f22134533`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 18.0 MB (18000429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6022bb89098191f5e257aa4e32bcfa33c5ad77af1820164d53a2d23a155c1efb`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e5a5238bf0b1dc3a4eee05c5847d1c25e2d05a3872672ff9030a6e39564f2`  
		Last Modified: Wed, 04 Dec 2024 00:29:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e341b6cbf0b1d0892b191cafb94e2bb674ea7086b15fb46fddcfc0a87a0950`  
		Last Modified: Wed, 04 Dec 2024 00:29:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37118131d8c6abc8a1d2bc3d06b19e716aba85bd70ef596e731912b3263caf68`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 9.1 MB (9060142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808ad8667e97e661f5dbf6ef2725dc1e89602f0c51f25e110c1d5d182a490c6`  
		Last Modified: Wed, 04 Dec 2024 01:28:49 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11440987ff8e3e813048fee3b7b704ec574022260dbe66591f9cd4b8c43dcd9c`  
		Last Modified: Wed, 04 Dec 2024 01:28:49 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c7b913e1f09d88e471b3909933b4992191770bb8f0d7987e9407b55d8f4b29`  
		Last Modified: Wed, 04 Dec 2024 01:28:52 GMT  
		Size: 53.5 MB (53511021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad8d0c2d6a8178e298e85ba96d6d2718f7046df88dfd0f2acf48946a20f6f1`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b4367498a260de054f3ab7caa2301f404535c5be8ceb9af00fc820a6d010a8`  
		Last Modified: Wed, 04 Dec 2024 01:28:50 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:0528ca2fa8acf242eac680e7dc3b059e769d47969412203ef9b30b692461f64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2eada113d5f4c8076d65858800c094e7761c0da275e0aeecccb35c15a583d83`

```dockerfile
```

-	Layers:
	-	`sha256:748bd2a8690fba2669cd29c9ba34cb8e69cbb5c5ca2a9e7b12ff0f0209d19674`  
		Last Modified: Wed, 04 Dec 2024 01:28:48 GMT  
		Size: 34.7 KB (34730 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:4282a706d0de62d1870d0748595012675b214e349123d04f8b28047f95fe7bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124083382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cd6b3959c6bdcfe0c15f185deaad456030912d24466023e92da5839f19c077`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a8d373266083cffcbf2a6623223d8b2c780180ffc25c641834fa0f399b861c`  
		Last Modified: Wed, 04 Dec 2024 07:15:41 GMT  
		Size: 7.2 MB (7153539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ecea7f1649dbef369192500f3eda21b1f30ba448ca4b382f6dc90ba4b77ed6`  
		Last Modified: Wed, 04 Dec 2024 07:15:40 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8345cbaadf649b7179d374408307a49de91dcad20d33264ff67e18f1df31ad`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 16.6 MB (16591541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0a479bcd6279df331f32a4aab4c0c1f2140ff8ad6863ac2e92df68745f4212`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 17.4 MB (17426318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bda8e0c337df3901bcac5c617da87c4374d34e45d2442c84e52a57079226`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 18.0 MB (17984726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922d604be17f4bbd00d6ed640b5b13212bb106fd9e1de0c22b96b23de6b53f8f`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f87b589e7a688691cd8e51d42d71f370527d4b4710084733eb6d3a885f95c8`  
		Last Modified: Wed, 04 Dec 2024 07:16:03 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dbeec76024b177d0212c7c8e652f88917461283d8538caf5e1b7120885f229`  
		Last Modified: Wed, 04 Dec 2024 07:16:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87469764160593846c30c8e28dac1080459b4051932d74fd34db73c0027d0565`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 8.2 MB (8228295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba34f50361e4b02b179eb03250dade6609581cc47552001b3b992c82798031d`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 84.5 KB (84498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a38bc738f51a41a50f63665a4183c459cf953d52052327d82e14c4fc2d069a`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38510939bc5659853d67592adbfba6d41d4f83a34c086b45ca197351df04db42`  
		Last Modified: Wed, 04 Dec 2024 09:58:59 GMT  
		Size: 53.5 MB (53511037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca93ad33ff91f6aaf58315b3c74581ce07d1f79488e6b309946a372f1928266`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cf7c178aa1938ea5f4c2b273d58b83721fe1c7133e13e05e37da3dd1b36839`  
		Last Modified: Wed, 04 Dec 2024 09:58:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:5060a914795d4ad7da1ec0b4baaa83c418aed4aa32a77f3269faa0676cf4ef54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56e35531d708cdb1857fb999b927304860627396f593f2f6bc9a5f8d9940760`

```dockerfile
```

-	Layers:
	-	`sha256:dda6401da3e01b40934462451eae7cf3f9e919ee3b1f51514bdb8af45a26d9dc`  
		Last Modified: Wed, 04 Dec 2024 09:58:57 GMT  
		Size: 34.7 KB (34730 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4d045d01ee7e2c931e74d17300e3e1994aa561841fc20f2323c64f36dcb6b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127617087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa4bd8f7eb76767555fa9b4fcfad991cb6ce4d97f38b7f5d83778b35ca10143`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4036cbb7a2e5b8a0ce714e4d08fbb64576b80cdd256ff9f0cba6473d73c3d`  
		Last Modified: Wed, 04 Dec 2024 01:35:25 GMT  
		Size: 8.0 MB (7998285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60d77d28745a9052470e2cbb96a13d33e0a0e02f2499098e3d150ae69df6ec1`  
		Last Modified: Wed, 04 Dec 2024 01:35:24 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91ef372941d329672b67f1838f7226808a97f8e58397715e78cd330e0868a9`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd17f2da053085769cb4bd5050acf30ee866b24423db4f6a4501542ff3c577e`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.1 MB (17094301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bf40ee41c170bda856abc36f41024d06b357a9952ada38b13eaa38f5e4fb42`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 17.5 MB (17533136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28d3c43303886712330874ba9a1a16c23148a9c3d9473bf8a713a8daaa7fab`  
		Last Modified: Wed, 04 Dec 2024 01:35:43 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37013ffc205c5864e92c2dcb7e0f270522f1567a8aa872a4387741223a709686`  
		Last Modified: Wed, 04 Dec 2024 01:35:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ffff7c773efbee73c878f22b1180466f0913d6bf9c789fc84e7327463c4b72`  
		Last Modified: Wed, 04 Dec 2024 01:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91e6f6ccb3fb7cbb88f239f42c64aada23404c0c4dce018a70293397b6a7bb2`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 9.9 MB (9854884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b149a083ef4ec99e387305c4f67b50322dca8423ae3768a35f45a2fd271e4f`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 98.7 KB (98661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ba97446cb2349c7c7ede5bac8c57eb62af7c4ed374b72d5c63231122fd3f3e`  
		Last Modified: Wed, 04 Dec 2024 05:06:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c66d82acbf0c58afe05ed4bd7a0e5537ad2a7247cc27a922ca66d5aa62748`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487d2d57a72d0f05061f16b8670991e34849ece621911b2e3501cab1ed7f5ea9`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86120177f87d9b796dce95a7af9473e7763db7ce5380f3ef778d258d244a6c3d`  
		Last Modified: Wed, 04 Dec 2024 05:06:40 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:53bbd101f17d09cd1cfbce5f9d4ae4d10faf7dea03558020c7bc7b0841655918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239273cc8f9eddd75eaf9bb9f6385ed96d3efeb918b400d9f49b8566fa417e8d`

```dockerfile
```

-	Layers:
	-	`sha256:e8f2b79a35f2afff1c0161dc8445fc1323b9a1ee36026f95eebda18988ec71dc`  
		Last Modified: Wed, 04 Dec 2024 05:06:38 GMT  
		Size: 34.8 KB (34790 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:a9b533ad3897a104820d026bf803f1961f7a5878421714a612247124d0acef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull docker@sha256:8f9c48d09df59573b09228e9dbfe3c594742424cae7426a5a35e8cc7aa3b36c4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311481903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97457ae6f523445fb75426553bfe303fced59f9220ae078d7e4c87715d45fc5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 04 Dec 2024 00:29:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Dec 2024 00:29:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Dec 2024 00:29:23 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 04 Dec 2024 00:29:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 04 Dec 2024 00:29:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:29:33 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 00:29:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Wed, 04 Dec 2024 00:29:34 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Wed, 04 Dec 2024 00:29:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:29:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 00:29:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 04 Dec 2024 00:29:45 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 04 Dec 2024 00:29:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8cf801ea0b73e0642e0b4ce32164423c74578a15913ce3c1522455550a51dc`  
		Last Modified: Wed, 04 Dec 2024 00:30:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce32181c8d548c5f3d5c7f21d6c1b4c138f11930d3b7148aca72a20670d60ef8`  
		Last Modified: Wed, 04 Dec 2024 00:30:02 GMT  
		Size: 368.7 KB (368664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6383050bfd01e5a60b58e3afe6ec6d1727c6c572e4ae362fb203f6547a3d36ba`  
		Last Modified: Wed, 04 Dec 2024 00:30:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3b0dbd135c9afcb2d3a67cf6793d6b0105763d826d910b5be9f56306cf0699`  
		Last Modified: Wed, 04 Dec 2024 00:30:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b486b2b85df328dd041bb776e8189405348f40be4026b361979170287dbf83`  
		Last Modified: Wed, 04 Dec 2024 00:30:04 GMT  
		Size: 18.9 MB (18895345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a797eeea5ccf96cfa615e788b8c83761178eaec7b197ce58af1f7617f1f47bf1`  
		Last Modified: Wed, 04 Dec 2024 00:30:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d270eee49201dcbef13d72f80110cf8520fe216813b9dbbd77a7bccb0671cb`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa40b1420cb32241d443d54fcb9c66295fc1614b803dd2b64b85b8045e88f83`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdec4827b0809606345cd494f89179f7a6a4bfa53c66de763707cc7a8a51a69b`  
		Last Modified: Wed, 04 Dec 2024 00:30:00 GMT  
		Size: 19.7 MB (19654760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b138a6306b3265d89ccf4b591674811e587f9f015dc00aa72e46fb90a33a43`  
		Last Modified: Wed, 04 Dec 2024 00:29:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ff6d4acbb626052eaf329cc2b79f40f95d3ea7e6c9dcd9fc0096b1468e0438`  
		Last Modified: Wed, 04 Dec 2024 00:29:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c8eb7eb52107738c2ba26a34591f105b95d2313a00e6000ae6e8f6722398e9`  
		Last Modified: Wed, 04 Dec 2024 00:29:56 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff881f29ea45eed545b1bee34dead2669cdfd435ecee8af251e2c4265367496d`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 20.1 MB (20067322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull docker@sha256:a2f5603c325e20bc846be7390f49f6dd7324812808f488f3e72bc9dde2f96d57
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2069734614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4603a9f3517e481eeec493fb07aa7eb2eeb779ce43cb2e34606b68efb8e8a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 04 Dec 2024 00:29:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Dec 2024 00:29:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Dec 2024 00:29:50 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 04 Dec 2024 00:29:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 04 Dec 2024 00:30:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:07 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 00:30:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Wed, 04 Dec 2024 00:30:08 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Wed, 04 Dec 2024 00:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 00:30:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 04 Dec 2024 00:30:22 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 04 Dec 2024 00:30:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c8c0d9c38caabebe3b73ab4c6eba8436f7f6362870802faa333902e268fda5`  
		Last Modified: Wed, 04 Dec 2024 00:30:42 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2a635d22c65bd08f6832968bbaf45742dcea846553e69cd5fb73524892186`  
		Last Modified: Wed, 04 Dec 2024 00:30:42 GMT  
		Size: 488.7 KB (488667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec026becc11bd18a346a2f61ef141260e67d4d5c5275e554a9668f99a60e2696`  
		Last Modified: Wed, 04 Dec 2024 00:30:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437214d0ea2a048e24dd206aecfeccb6ce5ccb823890b1ca8feb925dda2c9dd`  
		Last Modified: Wed, 04 Dec 2024 00:30:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4425edecd3624e76b516e6a14bf2381a3228b5b0cd0ca91f5b52242f0b761f52`  
		Last Modified: Wed, 04 Dec 2024 00:30:43 GMT  
		Size: 18.9 MB (18886052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8c997f46007664e2420e190bd026b2d3c615f2f092e4db109bcb66fbc2c230`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b692b1d417f77186832f783e691e3886c3b8473566614323f8090f22aaf482ef`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb109cfc2d9438feb076d8b232441c406096b2b98b39bdc3d6c8b71cff4a6f8f`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76412645838ed469d125fe7cbb4ee913c5e077868700d13338ed009778d34bb4`  
		Last Modified: Wed, 04 Dec 2024 00:30:40 GMT  
		Size: 19.6 MB (19644914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4314d510cc852d692dd9c73cb48da4c06607bf2426a12a710a1f7f23168cf6a8`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e08b405dd71ce49510066489c12e9c6d278bb87ddfce055c2ea7a51a7a1ea67`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61005e57942a2a801aafe59b869523568ec1b842f394fd1d5881b321422de2`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627830bfad7c6a2e11305e97939175b7844471db27f68b649091073c61f7f394`  
		Last Modified: Wed, 04 Dec 2024 00:30:40 GMT  
		Size: 20.0 MB (20049522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:f06d2055c2e10f622d21e2227032bf6ecba6d0b6444ba17059b7e4c822a3c9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull docker@sha256:a2f5603c325e20bc846be7390f49f6dd7324812808f488f3e72bc9dde2f96d57
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2069734614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4603a9f3517e481eeec493fb07aa7eb2eeb779ce43cb2e34606b68efb8e8a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 04 Dec 2024 00:29:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Dec 2024 00:29:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Dec 2024 00:29:50 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 04 Dec 2024 00:29:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 04 Dec 2024 00:30:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:07 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 00:30:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Wed, 04 Dec 2024 00:30:08 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Wed, 04 Dec 2024 00:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 00:30:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 04 Dec 2024 00:30:22 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 04 Dec 2024 00:30:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c8c0d9c38caabebe3b73ab4c6eba8436f7f6362870802faa333902e268fda5`  
		Last Modified: Wed, 04 Dec 2024 00:30:42 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2a635d22c65bd08f6832968bbaf45742dcea846553e69cd5fb73524892186`  
		Last Modified: Wed, 04 Dec 2024 00:30:42 GMT  
		Size: 488.7 KB (488667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec026becc11bd18a346a2f61ef141260e67d4d5c5275e554a9668f99a60e2696`  
		Last Modified: Wed, 04 Dec 2024 00:30:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437214d0ea2a048e24dd206aecfeccb6ce5ccb823890b1ca8feb925dda2c9dd`  
		Last Modified: Wed, 04 Dec 2024 00:30:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4425edecd3624e76b516e6a14bf2381a3228b5b0cd0ca91f5b52242f0b761f52`  
		Last Modified: Wed, 04 Dec 2024 00:30:43 GMT  
		Size: 18.9 MB (18886052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8c997f46007664e2420e190bd026b2d3c615f2f092e4db109bcb66fbc2c230`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b692b1d417f77186832f783e691e3886c3b8473566614323f8090f22aaf482ef`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb109cfc2d9438feb076d8b232441c406096b2b98b39bdc3d6c8b71cff4a6f8f`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76412645838ed469d125fe7cbb4ee913c5e077868700d13338ed009778d34bb4`  
		Last Modified: Wed, 04 Dec 2024 00:30:40 GMT  
		Size: 19.6 MB (19644914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4314d510cc852d692dd9c73cb48da4c06607bf2426a12a710a1f7f23168cf6a8`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e08b405dd71ce49510066489c12e9c6d278bb87ddfce055c2ea7a51a7a1ea67`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61005e57942a2a801aafe59b869523568ec1b842f394fd1d5881b321422de2`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627830bfad7c6a2e11305e97939175b7844471db27f68b649091073c61f7f394`  
		Last Modified: Wed, 04 Dec 2024 00:30:40 GMT  
		Size: 20.0 MB (20049522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9660f39af1699dd42956f5c43ab9d1f0e7229bbfce8129b52fa0cd9fde98d042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull docker@sha256:8f9c48d09df59573b09228e9dbfe3c594742424cae7426a5a35e8cc7aa3b36c4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311481903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97457ae6f523445fb75426553bfe303fced59f9220ae078d7e4c87715d45fc5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 04 Dec 2024 00:29:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Dec 2024 00:29:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Dec 2024 00:29:23 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 04 Dec 2024 00:29:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 04 Dec 2024 00:29:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:29:33 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 00:29:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Wed, 04 Dec 2024 00:29:34 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Wed, 04 Dec 2024 00:29:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:29:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 00:29:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 04 Dec 2024 00:29:45 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 04 Dec 2024 00:29:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8cf801ea0b73e0642e0b4ce32164423c74578a15913ce3c1522455550a51dc`  
		Last Modified: Wed, 04 Dec 2024 00:30:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce32181c8d548c5f3d5c7f21d6c1b4c138f11930d3b7148aca72a20670d60ef8`  
		Last Modified: Wed, 04 Dec 2024 00:30:02 GMT  
		Size: 368.7 KB (368664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6383050bfd01e5a60b58e3afe6ec6d1727c6c572e4ae362fb203f6547a3d36ba`  
		Last Modified: Wed, 04 Dec 2024 00:30:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3b0dbd135c9afcb2d3a67cf6793d6b0105763d826d910b5be9f56306cf0699`  
		Last Modified: Wed, 04 Dec 2024 00:30:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b486b2b85df328dd041bb776e8189405348f40be4026b361979170287dbf83`  
		Last Modified: Wed, 04 Dec 2024 00:30:04 GMT  
		Size: 18.9 MB (18895345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a797eeea5ccf96cfa615e788b8c83761178eaec7b197ce58af1f7617f1f47bf1`  
		Last Modified: Wed, 04 Dec 2024 00:30:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d270eee49201dcbef13d72f80110cf8520fe216813b9dbbd77a7bccb0671cb`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa40b1420cb32241d443d54fcb9c66295fc1614b803dd2b64b85b8045e88f83`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdec4827b0809606345cd494f89179f7a6a4bfa53c66de763707cc7a8a51a69b`  
		Last Modified: Wed, 04 Dec 2024 00:30:00 GMT  
		Size: 19.7 MB (19654760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b138a6306b3265d89ccf4b591674811e587f9f015dc00aa72e46fb90a33a43`  
		Last Modified: Wed, 04 Dec 2024 00:29:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ff6d4acbb626052eaf329cc2b79f40f95d3ea7e6c9dcd9fc0096b1468e0438`  
		Last Modified: Wed, 04 Dec 2024 00:29:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c8eb7eb52107738c2ba26a34591f105b95d2313a00e6000ae6e8f6722398e9`  
		Last Modified: Wed, 04 Dec 2024 00:29:56 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff881f29ea45eed545b1bee34dead2669cdfd435ecee8af251e2c4265367496d`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 20.1 MB (20067322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
